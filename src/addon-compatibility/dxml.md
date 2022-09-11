# DXML

## Intro

DXML by demonized#1084

DXML is a part of modded exes repo ([https://github.com/themrdemonized/STALKER-Anomaly-modded-exes](https://github.com/themrdemonized/STALKER-Anomaly-modded-exes))

DXML allows to manipulate XML files before they loaded into the engine or scripts by utilizing Lua
The engine sends XML string to Lua where it is transformed into DOM-like object (from now on lets call it xml_obj) that can be manipulated by Lua methods and then it is converted back to XML string and sent back to engine

To use it in your mods, you have to create a new script file that is called `modxml_<yourname>.script`. The yourname can be any string, it doesnt matter. The "modxml_" part must be in the filename.

Then, in this file, type:

```lua
function on_xml_read()
    RegisterScriptCallback("on_xml_read", function(xml_file_name, xml_obj)
        -- XML file i want to change
        local xml_to_change = [[text\eng\_game_version.xml]]

        -- Check if its the file i want to change
        if xml_file_name == xml_to_change then
            -- Here is my code to change XML
        end
    end)
end
```

What this does is creating a function on_xml_read that will be auto-called from _g.script. This function will register function for new callback "on_xml_read", which accepts two arguments:

* xml_file_name - current XML filename that engine is processing (for example: text\eng\_game_version.xml)
* xml_obj - the object described above

To understand, what can be done with xml_obj and what functions it provides, let's take a look at typical usecases:

### Case 1: inserting new XML data

**Examples: insert new dialog into gameplay\dialogs.xml, insert new scope texture into ui\scopes.xml**

This is the simplest case of using DXML, where you just want to insert new data, much like `#include` directive in XML files

To do this, you can use `xml_obj:insertFromXMLString` function as in example below:

```lua
function on_xml_read()
    RegisterScriptCallback("on_xml_read", function(xml_file_name, xml_obj)
        -- XML file i want to change
        local xml_to_change = [[ui\scopes.xml]]

        -- Check if its the file i want to change
        if xml_file_name == xml_to_change then
            -- Here is my code to change XML
            local my_new_scope = 
[[
<wpn_crosshair_bino x="0" y="0" width="2048" height="1536">
    <auto_static x="0" y="0" width="1024" height="768" stretch="1">
    <texture>wpn_crosshair_bino</texture>
    </auto_static>
</wpn_crosshair_bino>
]]
            xml_obj:insertFromXMLString(my_new_scope)
        end
    end)
end
```

This example adds new scope texture into scopes.xml.

insertFromXMLString method has these arguments:

* "xml_string" - XML string to process
* "where" - the element in xml_obj in which new data will be inserted argument is optional and specifies an element subtable of self.xml_table to insert (default - root element)
* "pos" argument is optional and specifies position to insert (default - to the end)

The function returns the position of first inserted element in "where"

## Case 2: inserting new XML data in specified element

**Example: insert new menu item into ui\ui_mm_main.xml**

In order to correctly insert new main menu item, we need to find the <menu_main> element first.

To find an element, you can utilize CSS-like selectors in `query` function. An example of finding <menu_main> element would be:

```lua
local res = xml_obj:query("menu_main")
```

The function returns a table with all found elements matching this query.

The element is represented by table with following fields:

* el = element type, consists of type symbol, name and attributes. The type symbols are:
  * "<" - node element
  * "#" - text element
* parent = pointer to a table that contains this element
* kids = table that contains all children of this element

Then we check if table is not empty (the element exists) and insert our xml string with new menu item in position before the end

```lua
if is_not_empty(res) then
    local el = res[1]
    xml_obj:insertFromXMLString([[<btn name="btn_mcm" caption="ui_mm_menu_mcm"/>]], el, #el.kids)
```

Full code would be:

```lua
function on_xml_read()
    RegisterScriptCallback("on_xml_read", function(xml_file_name, xml_obj)
        -- XML file i want to change
        local xml_to_change = [[ui\ui_mm_main.xml]]

        -- Check if its the file i want to change
        if xml_file_name == xml_to_change then
            -- Here is my code to change XML
            local mcm_menu = [[<btn name="btn_mcm" caption="ui_mm_menu_mcm" />]]
            local res = xml_obj:query("menu_main")
            if is_not_empty(res) then
                local el = res[1]
                xml_obj:insertFromXMLString(mcm_menu, el, #el.kids)
            end
        end
    end)
end
```

But, if there is already an MCM menu, then you might get duplicated element inside. So we have to check if its already exists before insertion. We can check if element `<btn name="btn_mcm">` exists before proceeding by utilizing `query` again.

Here, similar to CSS, we want to find `<btn>` element with attribute `name="btn_mcm"` first. if its found - then make early return from the function

```lua
    if is_not_empty(xml_obj:query("menu_main btn[name=btn_mcm]")) then
        printf("MCM button already exists")
        return
    end
```

Full list of available CSS-like selectors are:

* " " (space) - find children of elemenents (can be any depth inside)
* ">" - find direct children
* "+" - find first sibling of element
* "~" - find all siblings
* "[attr1=value1]" - describes attribute `attr1` with value `value1`. To find element that matches multiple attributes you can use `[attr1=value1][attr2=value2]` and so on

## Case 3: Change text inside element

**Example: change text of game version in text\eng\\_game_version.xml**

Getting and setting text is possible if element contains raw text inside, like `<text attr1="value1">My Text</text>`.
To get text, you can use `getText(element)` function and to set it use `setText(element)`.
Example below of appending text to existing text in element

```lua
function on_xml_read()
	RegisterScriptCallback("on_xml_read", function(xml_file_name, xml_obj)
		if xml_file_name == [[text\eng\_game_version.xml]]
		or xml_file_name == [[text\rus\_game_version.xml]]
		then
			-- Find string element with "id=ui_st_game_version" text inside it
			local res = xml_obj:query("string[id=ui_st_game_version] > text")
			if res[1] then
				el = res[1]
				local el_text = xml_obj:getText(el)
				if el_text then
					-- Set new text
					xml_obj:setText(el, el_text .. ". Modified exes (DLTX, DXML, Shader Scopes, SSS)")
				end
			end
		end
	end)
end
```

## Case 4: changing attribute of element

**Example: change position of money display in ui\ui_inventory.xml**

First, find `<money>` element inside `<player>` element and then change its x, y attributes by using `setElementAttr` function

`setElementAttr(el, args)`

* el - element found using `query`
* args - table of attributes ({attr1 = value1, attr2 = value2})

To get attributes of element, use `getElementAttr` function, it returns a table of attributes described above

`getElementAttr(el)`

* el - element found using `query`

To remove attributes of element, use `removeElementAttr` function

`removeElementAttr(el, args)`

* el - element found using `query`
* args - list of attributes to remove ({attr1, attr2})

```lua
function on_xml_read()
	RegisterScriptCallback("on_xml_read", function(xml_file_name, xml_obj)
		if xml_file_name == [[ui\ui_inventory.xml]]
		then
			-- Find string element with "id=ui_st_game_version" text inside it
			local res = xml_obj:query("player > money")
			if res[1] then
				el = res[1]
				xml_obj:setElementAttr(el, {x=20, y=60})
			end
		end
	end)
end
```

## PS

Full list of methods is described in _g.script in `COnXmlRead` function