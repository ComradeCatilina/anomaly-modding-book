# Console commands

___

## About

This section describes all console commands.

All the settings described below are stored in the file "user".ltx. (You can read more about [important files here](../main-folders-and-files/index.html))

### Game

| Сommand | Command description | Command's argument | Note |
---|---|:---:|---|
| help | Outputs a list of console commands | - | - |
| g_dead_body_collision | Enables collision | full<br> actor_only<br> off | - |
| g_game_difficulty | Selects the game difficulty | gd_novice<br> gd_stalker<br> gd_veteran<br> gd_master |  |
| g_god | Enables God Mode | 'on/off' or '1/0' | - |
| g_hit_pwr_modif | Bone damage modifier | 0.500 - 3.000 | - |
| g_ironsights_zoom_factor | Zoom factor of the mechanical sight | 1.000 - 2.000 | - |
| g_unlimitedammo | Enables Infinite Ammo Mode | 'on/off' or '1/0' | - |
| g_use_tracers |  | 'on/off' or '1/0' | - |
| g_important_save | Saving at key points | 'on/off' or '1/0' | - |
| g_autopickup | Enables the ability to pick up items automatically | 'on/off' or '1/0' | Not working |
| g_always_active | The game will continue to work if the focus is not on it | 'on/off' or '1/0' | - |
| demo_play | Plays the selected demo_record | "name" of demo | - |
| demo_record | Enables recording of camera overflights | "name" of demo | Space bar sets key points when the camera flies<br> <br>The Enter key exits record mode and takes the player to the exit point from demo_record mode |
| demo_set_cam_position |  |  | - |
| keypress_on_start | Whether to wait after loading a level to press the key to go into the game | 'on/off' or '1/0' | - |
| load | Load specified save | save_name | - |
| load_last_save | Load last save | - | - |
| main_menu | Exit to the main menu | - | - |
| quit | Exit to the desktop | - | - |
| cl_cod_pickup_mode | Selecting items from the radius around the scope | 'on/off' or '1/0' | - |
| disconnect | Ends the game | - | - |
| time_factor | Ability to change the game time | 0.001 - 1000.0 | - |
| jump_to_level | Moving to the selected level | k00_marsh<br> l01_escape<br> l02_garbage<br> l03_agroprom<br> k01_darkscape<br> l04_darkvalley<br> l05_bar<br> l06_rostok<br> l07_military<br> l08_yantar<br> l09_deadcity<br> l10_limansk<br> l10_radar<br> l10_red_forest<br> l11_hospital<br> l11_pripyat<br> l12_stancia<br> l12_stancia_2<br> l13_generators<br> l03u_agr_underground<br> l04u_labx18<br> l08u_brainlab<br> l10u_bunker<br> l12u_sarcofag<br> l12u_control_monolith<br> l13u_warlab<br> zaton<br> jupiter<br> jupiter_underground<br> pripyat<br> labx8<br> k02_truck_cemetery<br> fake_start<br> y04_pole | - |

#### Actor

| Сommand | Command description | Command's argument |
---|---|:---:|
| head_bob_factor | Basic head bobbing factor | 0 - 2 |

#### HUD

| Сommand | Command description | Command's argument |
---|---|:---:|
| g_simple_pda |  | 'on/off' or '1/0' |
| g_3d_pda | Switching between 2D and 3D PDA modes | 'on/off' or '1/0' |
| hud_weapon | Shows weapons and hands | 'on/off' or '1/0' |
| hud_draw | Shows UI | 'on/off' or '1/0' |
| hud_fov | FOV for HUD | 0.100 - 1.000 |

#### UI

| Сommand | Command description | Command's argument | Note |
---|---|:---:|---|
| cl_dynamiccrosshair | Dynamic Sight | 'on/off' or '1/0' | Not working because of the dot sight |
| g_crosshair_color | Changes the color of the crosshair | (0 - 255, 0 - 255, 0 - 255, 0 - 255) | Argument is taken in [RGBA](https://en.wikipedia.org/wiki/RGBA_color_model) format<br> <br>First value (0 - 255) - Red</br> Second value (0 - 255) - Green<br> Third value (0 - 255) - Blue<br> Fourth value (0 - 255) - Alpha |
| g_feel_grenade | "Sensitivity" grenade | 'on/off' or '1/0' | - |
| hud_crosshair | Show crosshair | 'on/off' or '1/0' | - |
| hud_crosshair_dist | Show distance to target under crosshair | 'on/off' or '1/0' | - |

#### Debug

| Сommand | Command description | Command's argument |
---|---|:---:|
| rs_stats | Display engine statistics on the screen | 'on/off' or '1/0' |
| rs_cam_pos | Display camera coordinates | 'on/off' or '1/0' |
| list_actions | Display a list of active console commands | - |
| bind_list | Display a list of commands assigned to the keys | - |
| hud_info |  | - |
| render_memory_stats | Output information about memory usage | - |
| stat_memory |  | - |

### Control

| Сommand | Command description | Command's argument | Note |
---|---|:---:|---|
| bind | Assign a command to the button | Action, key prefixed with k (kLeft, etc.) | - |
| mouse_invert | Inverts the mouse | 'on/off' or '1/0' | - |
| mouse_sens | Mouse sensitivity | 0.001 - 0.600 | - |
| mouse_sens_aim | Mouse sensitivity when aiming | 0.500 - 2.000 | - |
| default_controls | Resets key settings to defaults | - | - |
| wpn_aim_toggle | Aiming Mode | 'on/off' or '1/0' | - |
| g_backrun | Backward running mode | 'on/off' or '1/0' | Not working |
| g_crouch_toggle | Sit/stand mode | 'on/off' or '1/0' | - |
| g_sprint_toggle | Sprint mode | 'on/off' or '1/0' | - |
| g_walk_toggle |  | 'on/off' or '1/0' | - |

### Discord

| Сommand | Command description | Command's argument |
---|---|:---:|
| discord_status | Displays status in Discord | 'on/off' or '1/0' |
| discord_update_rate | Discord update rate | 0.500 - 5.000 |

### Sound

#### General settings

| Сommand | Command description | Command's argument |
---|---|:---:|
| snd_restart | Restart the sound engine | — |
| snd_cache_size | Cache size | 8 - 256 |
| snd_acceleration | APU resource utilization | 'on/off' or '1/0' |
| snd_targets | Maximum number of channels | 32 - 1024 |
| snd_device |  | OpenAL Soft |

#### Music

| Сommand | Command description | Command's argument | Note |
---|---|:---:|---|
| snd_volume_eff | Volume of sounds | 0.000 - 1.000 | - |
| snd_volume_music | Music volume | 0.000 - 1.000 | - |
| g_dynamic_music | Turns on dynamic music (during firefights) | 'on/off' or '1/0' | In the game the script `xrs_dyn_music.script` responsible for playing music is corrupted. An addon restoring this script can help to fix it (Example: [COMBAT MUSIC RESTORED + EXTENDED](https://www.moddb.com/mods/stalker-anomaly/addons/combat-music-restored-extended)) |

#### Effects

| Сommand | Command description | Command's argument |
---|---|:---:|
| snd_efx | EAX sound effects | 'on/off' or '1/0' |

### Physics

| Сommand | Command description | Command's argument |
---|---|:---:|
| ph_gravity | Gravity | 0.000 - 1000.000 |
| ph_frequency | The more, the better the collision calculations | 50.0000 - 200.0000 |
| ph_iterations | Number of iterations to calculate the dynamics | 15 - 50 |

### Camera

| Сommand | Command description | Command's argument |
---|---|:---:|
| cam_inert | Camera inertia | 0.000 - 1.000 |
| cam_slide_inert |  | 0.000 - 1.000 |
| fov | FOV for camera | 5.000 - 180.000 |

### Graphics

#### Graphics General settings

| Сommand | Command description | Command's argument |
---|---|:---:|
| _preset | Selecting a set of quality settings | Minimum<br> Low<br> Default<br> High/Extreme |
| rs_screenmode | Resolution selection mode | Windowed<br> Fullscreen<br> Borderless<br> Windowed |
| rs_v_sync | Vertical Sync | 'on/off' or '1/0' |
| rs_refresh_60hz | Screen refresh rate 60 Hz | 'on/off' or '1/0' |

#### Renders

##### Common commands for all renders

| Сommand | Command description | Command's argument |
---|---|:---:|
| renderer | Render type (old) |  |
| rs_vis_distance | Visibility range | 0.400 - 1.500 |
| r__actor_shadow | Player shadow | 'on/off' or '1/0' |
| r__bloom_thresh | Brightness threshold for 3rd party bloom shader | 0.0 - 1.0 |
| r__bloom_weight | Bloom weights for 3rd party bloom shader | 0.0 - 1.0 |
| r__clear_models_on_unload |  | 'on/off' or '1/0' |
| r__color_grading |  | 0.000000e+00, 0.000000e+00, 0.000000e+00 - 1.000000e+00, 1.000000e+00, 1.000000e+00 |
| r__detail_density | Grass density | 0.040 - 1.000 |
| r__detail_height | Grass height | 0.5 - 2.0 |
| r__detail_radius | Grass rendering radius | 50.0 - 250.0 |
| r__dtex_range |  | 5.000 - 175.000 |
| r__enable_grass_shadow | Enables grass shadows | 'on/off' or '1/0' |
| r__exposure | Scene exposure | 0.500 - 4.000 |
| r__framelimit | FPS limiter | 0 - 500 |
| r__gamma | Scene gamma | 0.500 - 2.200 |
| r__geometry_lod | Geometry level of detail | 0.100 - 1.500 |
| r__lens_flares | The "lens flare" effect | 'on/off' or '1/0' |
| r__nightvision | Controls nightvision shader | 0 - 3 |
| r__no_ram_textures |  | 'on/off' or '1/0' |
| r__no_scale_on_fade |  | 'on/off' or '1/0' |
| r__optimize_dynamic_geom |  | 0 - 4 |
| r__optimize_shadow_geom |  | 'on/off' or '1/0' |
| r__optimize_static_geom |  | 0 - 4 |
| r__saturation | Color saturation | 0.0 - 2.0 |
| r__supersample | Supersampling (DX8) | 1 - 8 |
| r__tf_aniso | Anisotropic filtering | 0<br> 4<br> 8<br> 16 |
| r__tf_mipbias | bias for initial texture mip level | -3.0 - 3.0 |
| r__use_precompiled_shaders |  | 'on/off' or '1/0' |
| r__wallmark_ttl | Wallmark Lifetime | 1.000 - 600.000 |
| r_screenshot_mode | Screenshot in the selected format | jpg<br> png<br> tga |

##### R1 - SM2.0 (DX9.0)

| Сommand | Command description | Command's argument |
---|---|:---:|
| r1_detail_textures | Detailed textures on static lighting | 'on/off' or '1/0' |
| r1_dlights | Dynamic light sources on static lighting | 'on/off' or '1/0' |
| r1_dlights_clip | Sets the display radius (visibility range) of dynamic light sources | 10.000 - 150.000 |
| r1_fog_luminance | Fog brightness | 0.2 - 5.0 |
| r1_glows_per_frame | Controls the maximum number of light sources | 2 - 32 |
| r1_lmodel_lerp | Controls Linear Lighting Interpolation | 0.000 - 0.333 |
| r1_pps_u | Controls Per Pixel Shader value | -1.000 - 1.000 |
| r1_pps_v | Controls Per Pixel Shader value | -1.000 - 1.000 |
| r1_software_skinning |  | 0 - 2 |
| r1_ssa_lod_a | Controls the level of detail (LOD) in the game world | 16.000 - 96.000 |
| r1_ssa_lod_b | Controls the level of detail (LOD) in the game world | 16.000 - 64.000 |

##### R2 - SM3.0 (DX9.0c)

| Сommand | Command description | Command's argument |
---|---|:---:|
| r2_aa | "Pseudo-smoothing" on dynamic lighting | 'on/off' or '1/0' |
| r2_aa_break | Distance at which the "Pseudo-smoothing" effect works | 0.000000e+00, 0.000000e+00, 0.000000e+00 - 1.000000e+00, 1.000000e+00, 1.000000e+00 |
| r2_aa_kernel | The basic value of the "Pseudo-smoothing" effect | 0.300 - 0.700 |
| r2_aa_weight | Controls the blurring of the fake AA more accurately | 0.000000e+00, 0.000000e+00, 0.000000e+00 - 1.000000e+00, 1.000000e+00, 1.000000e+00 |
| r2_allow_r1_lights |  | 'on/off' or '1/0' |
| r2_detail_bump | Detail textures | 'on/off' or '1/0' |
| r2_dof |  |  |
| r2_dof_enable | Enables depth of field | 'on/off' or '1/0' |
| r2_dof_radius | Doesn't work. In vanilla game that command controls blur radius | 0.05 - 1.0 |
| r2_dof_sky | Sky depth | -10000.0 - 10000.0 |
| r2_drops_control | Controls rain drops shader | 0.000000e+00, 0.000000e+00, 0.000000e+00 - 1.000000e+00, 2.000000e+00, 1.000000e+00 |
| r2_exp_donttest_shad |  | 'on/off' or '1/0' |
| r2_gi | Global illumination | 'on/off' or '1/0' |
| r2_gi_clip | Global illumination effect range | 0.000 - 0.100 |
| r2_gi_depth | Shadow depth of the global illumination effect | 1 - 5 |
| r2_gi_photons | Number of rays to trace the global illumination effect | 8 - 256 |
| r2_gi_refl | Reflectivity of global illumination effect surfaces | 0.001 - 0.990 |
| r2_gloss_factor | Surface gloss level | 0.001 - 10.000 |
| r2_gloss_min | Minimal gloss level | 0.001 - 1.0 |
| r2_ls_bloom_fast | In theory, this should enable faster bloom implementation, yet it doesn't work correctly | 'on/off' or '1/0' |
| r2_ls_bloom_kernel_b | Determines the level of shading (haze) from the HDR and Bloom | 0.010 - 1.000 |
| r2_ls_bloom_kernel_g | Bloom 'radius'. Higher values results in softer bloom | 1.0 - 7.0 |
| r2_ls_bloom_kernel_scale | Bloom scale | 0.05 - 2.0 |
| r2_ls_bloom_speed |  | 0.000 - 100.000 |
| r2_ls_bloom_threshold | Brightness threshold | 0.0 - 1.0 |
| r2_ls_depth_bias | Controls the range of light sources | -0.500 - 0.500 |
| r2_ls_depth_scale | Controls the effect of lighting on shadows | 0.500 - 1.500 |
| r2_ls_dsm_kernel |  | 0.100 - 3.000 |
| r2_ls_psm_kernel |  | 0.100 - 3.000 |
| r2_ls_squality |  | 0.500 - 1.000 |
| r2_ls_ssm_kernel |  | 0.100 - 3.000 |
| r2_mask_control | Controls gasmask shader | 0.000000e+00, 0.000000e+00, 0.000000e+00, 0.000000e+00 - 1.000000e+01, 3.000000e+00, 1.000000e+00, 1.000000e+00 |
| r2_mblur | Motion blur intensity | 0.0 - 1.0 |
| r2_mblur_enabled | Enables motion blur effect | 'on/off' or '1/0' |
| r2_parallax_h | Parallax strength | 0.0 - 0.5 |
| r2_qsync |  | 0 - 1 |
| r2_shadow_cascede_old | Enables 'SoC-like' shadow mapping | 'on/off' or '1/0' |
| r2_slight_fade |  | 0.200 - 1.000 |
| r2_smaa | Subpixel Morphological Anti-aliasing | off<br> low<br> medium<br> high<br> ultra |
| r2_soft_particles | Soft particles | 'on/off' or '1/0' |
| r2_soft_water | Soft Water | 'on/off' or '1/0' |
| r2_ss_sunshafts_length | Length of screen-space sun rays | 0.2 - 1.5 |
| r2_ss_sunshafts_radius |  | 0.500 - 2.000 |
| r2_ssa_lod_a | Level of detail of dynamic objects | 16.0 - 96.0 |
| r2_ssa_lod_b | Level of detail of static objects | 32.0 - 96.0 |
| r2_ssao | Screen space ambient occlusion effect quality | st_opt_off<br> st_opt_low<br> st_opt_medium<br> st_opt_high<br> st_opt_ultra |
| r2_ssao_blur | Doesn't work. | 'on/off' or '1/0' |
| r2_ssao_half_data | Enables half-resolution depth buffer for AO | 'on/off' or '1/0' |
| r2_ssao_hbao | Horizon-Based Ambient Occlusion | 'on/off' or '1/0' |
| r2_ssao_hdao | High-definition Ambient Occlusion | 'on/off' or '1/0' |
| r2_ssao_mode | Ambient occlusion type | disabled<br> default<br> hdao<br> hbao |
| r2_ssao_opt_data |  | 'on/off' or '1/0' |
| r2_steep_parallax | Steep parallax occlusion mapping | 'on/off' or '1/0' |
| r2_sun | Shadows from the sun | 'on/off' or '1/0' |
| r2_sun_depth_far_bias |  | -0.500 - 0.500 |
| r2_sun_depth_far_scale |  | 0.500 - 1.500 |
| r2_sun_depth_near_bias |  | -0.500 - 0.500 |
| r2_sun_depth_near_scale |  | 0.500 - 1.500 |
| r2_sun_details | Shadows of grass and other detailed objects | 'on/off' or '1/0' |
| r2_sun_far |  | 51.000 - 180.000 |
| r2_sun_focus | Focus of sun shadows | 'on/off' or '1/0' |
| r2_sun_lumscale | Sun light brightness | 0.0 - 3.0 |
| r2_sun_lumscale_amb | Ambient light brightness | 0.0 - 3.0 |
| r2_sun_lumscale_hemi | Sky light brightness | 0.0 - 3.0 |
| r2_sun_near | The location of the sun from the earth | 1.000 - 150.000 |
| r2_sun_near_border |  | 0.500 - 1.000 |
| r2_sun_quality | Shadow filter quality | st_opt_low<br> st_opt_medium<br> st_opt_high<br> st_opt_ultra<br> st_opt_extreme |
| r2_sun_tsm | Clarity of sun shadows | 'on/off' or '1/0' |
| r2_sun_tsm_bias |  | -0.500 - 0.500 |
| r2_sun_tsm_proj |  | 0.001 - 0.800 |
| r2_sunshafts_min | Min. sun rays intensity | 0.0 - 0.5 |
| r2_sunshafts_mode | Sun rays mode | off<br> volumetric<br> screen_space<br> combined |
| r2_sunshafts_quality | Quality of the sun rays | st_opt_low<br> st_opt_medium<br> st_opt_high |
| r2_sunshafts_value | Sun rays intensity | 0.0 - 2.0 |
| r2_terrain_z_prepass |  | 'on/off' or '1/0' |
| r2_tnmp_a |  | 0.0 - 20.0 |
| r2_tnmp_b |  | 0.0 - 20.0 |
| r2_tnmp_c |  | 0.0 - 20.0 |
| r2_tnmp_d |  | 0.0 - 20.0 |
| r2_tnmp_e |  | 0.0 - 20.0 |
| r2_tnmp_exposure | Tonemap exposure | 0.0 - 20.0 |
| r2_tnmp_f |  | 0.0 - 20.0 |
| r2_tnmp_gamma | Tonemap gamma | 0.0 - 20.0 |
| r2_tnmp_onoff | Enables custom tonemapping (based on Uncharted 2 curve) | 0.0 - 1.0 |
| r2_tnmp_w | White point | 0.0 - 20.0 |
| r2_tonemap | Enables eye-adaptation | 'on/off' or '1/0' |
| r2_tonemap_adaptation | Eye-adaptation speed | 0.0 - 10.0 |
| r2_tonemap_amount |  | 0.000 - 1.000 |
| r2_tonemap_lowlum | Controls the tone mapping effect on dark locations | 0.000 - 1.000 |
| r2_tonemap_middlegray | Controls the overall appearance of the HDR effect | 0.000 - 2.000 |
| r2_volumetric_lights | Volumetric light | 'on/off' or '1/0' |
| r2_wait_sleep |  | 0 - 1 |
| r2_water_reflections |  | 'on/off' or '1/0' |
| r2_zfill |  | 'on/off' or '1/0' |
| r2_zfill_depth |  | 0.001 - 0.500 |
| r2em |  | 0.000 - 4.000 |

##### R3 - SM4.0 (DX10) or SM4.1 (DX10.1)

| Сommand | Command description | Command's argument |
---|---|:---:|
| r3_dynamic_wet_surfaces | Wet surfaces | 'on/off' or '1/0' |
| r3_dynamic_wet_surfaces_far | Max. rendering distance of the effect | 30 - 100 |
| r3_dynamic_wet_surfaces_near | Min. rendering distance of the effect | 10 - 70 |
| r3_dynamic_wet_surfaces_sm_res | Resolution of rain 'shadowmap' | 64 - 2048 |
| r3_minmax_sm |  | on<br> off<br> auto<br> autodetect |
| r3_msaa | Multisample Anti-aliasing | st_opt_off<br> 2x<br> 4x<br> 8x |
| r3_msaa_alphatest | Alpha-test used with MSAA | st_opt_off<br> st_opt_atest_msaa_dx10_0<br> st_opt_atest_msaa_dx10_1 |
| r3_use_dx10_1 | Enables use of DX10.1 | 'on/off' or '1/0' |
| r3_volumetric_smoke | Volumetric smoke | 'on/off' or '1/0' |

##### R4 - SM5.0 (DX11)

| Сommand | Command description | Command's argument |
---|---|:---:|
| r4_enable_tessellation | Tessellation | 'on/off' or '1/0' |
| r4_wireframe | Displays the wireframe of dynamic models (not working) | 'on/off' or '1/0' |

#### Brightness-Contrast-Gamma

| Сommand | Command description | Command's argument | Note |
---|---|:---:|---|
| rs_c_brightness | Brightness | 0.500 - 1.500 | - |
| rs_c_contrast | Contrast | 0.500 - 1.500 | - |
| rs_c_gamma | Gamma | 0.500 - 1.500 | Not working |

#### Video

| Сommand | Command description | Command's argument |
---|---|:---:|
| vid_mode | Screen resolution | 800x600<br> 1024x768<br> 1280x720<br> 1280x1024<br> 1366x768<br> 1600x900<br> 1680x1050<br> 1920x1080 |
| vid_restart | Reboot the video engine | - |

#### Textures

| Сommand | Command description | Command's argument |
---|---|:---:|
| texture_lod | Texture detailing | 0 - 4 |

### AI

| Сommand | Command description | Command's argument |
---|---|:---:|
| ai_aim_max_angle | The maximum angle at which the angular velocity of the character when aiming is calculated by the formula | 0.000 - 31.416 |
| ai_aim_min_angle | The minimum angle at which the angular velocity of the character when aiming is calculated by the formula | 0.000 - 31.416 |
| ai_aim_min_speed | Minimum angular velocity of the character when aiming at a target | 0.000 - 31.416 |
| ai_aim_predict_time | Time of the character's prediction of a change in target position | 0.000 - 10.000 |
| ai_aim_use_smooth_aim |  | 'on/off' or '1/0' |
| ai_die_in_anomaly | Enables NPCs to die in anomalies | 'on/off' or '1/0' |
| ai_use_old_vision | Includes the old model of virtual character vision, in which random points on the surface of an ellipsoid inscribed into an axially oriented rectangular parallelepiped described around the object were taken to determine the visibility of the object. | 'on/off' or '1/0' |
| ai_use_torch_dynamic_lights | Enables the use of flashlights by non-player characters (NPCs) | 'on/off' or '1/0' |
