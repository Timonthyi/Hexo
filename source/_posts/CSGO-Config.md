---
title: CSGO-Config
date: 2020-07-26 22:17:21
tags:
categories: CSGO
---

# Common
~~~cfg
//灵敏度
sensitivity 2.0
zoom_sensitivity_ratio_mouse 1

//准心参数以及持枪视角
cl_crosshair_drawoutline "1"
cl_crosshair_dynamic_maxdist_splitratio "0.35"
cl_crosshair_dynamic_splitalpha_innermod "1"
cl_crosshair_dynamic_splitalpha_outermod "0.5"
cl_crosshair_dynamic_splitdist "7"
cl_crosshair_friendly_warning "1"
cl_crosshair_outlinethickness "1"
cl_crosshair_sniper_show_normal_inaccuracy "0"
cl_crosshair_sniper_width "1"
cl_crosshair_t "0"
cl_crosshairalpha "250"
cl_crosshaircolor "1"
cl_crosshaircolor_b "50"
cl_crosshaircolor_g "250"
cl_crosshaircolor_r "50"
cl_crosshairdot "0"
cl_crosshairgap "-0.130744"
cl_crosshairsize "2"
cl_crosshairstyle "4"
cl_crosshairthickness "0"
cl_crosshairusealpha "1"
cl_fixedcrosshairgap "3"
cl_viewmodel_shift_left_amt "0.500000"
cl_viewmodel_shift_right_amt "0.250000"
viewmodel_fov "63"
viewmodel_offset_x "1.5"
viewmodel_offset_y "2"
viewmodel_offset_z "-2﻿"
viewmodel_presetpos "0"
viewmodel_recoil "0"
cl_bob_lower_amt "5.000000"
cl_bobamt_lat "0.100000"
cl_bobamt_vert "0.100000"
cl_bobcycle "0.98"

viewmodel_recoil 0			//取消开枪枪口向上跳动


//基础设置
con_enable 1       			//开启控制台
con_enable 1       			//开启控制台[不用改]
fps_max 300         			//最大帧数
fps_max_menu 120   		//主界面最大帧数
engine_no_focus_sleep 50		//窗口失焦/在后台时掉帧省电	<50默认 0关闭>

net_graph 1      			//显示网络参数	<1.显示 2.隐藏>
net_graphpos 2     			//网络参数水平位置	<1.右 2.中 3.左>
net_graphheight 0     		//竖直方向高度
net_graphproportionalfont 0  	  	//字体大小		<0.缩小 1.正常>

cl_autowepswitch 0  			//关闭自动换上捡起的武器	P.S. 珍爱生命，远离自动换枪
cl_autohelp 0     			//禁用游戏提示（切换单发/三连发提示）
cl_showhelp 0     			//禁用游戏提示
cl_showpos 0			//不显示位置速度信息
cl_spec_follow_grenade_key 0		//手雷追踪键 <0.左ALT 1.左SHIFT 2.装弹键(R)>
cl_dm_buyrandomweapons 0	   	//关闭死斗随机买枪
cl_use_opens_buy_menu 0 		//关闭E键打开购买菜单
cl_crosshair_friendly_warning 1		//瞄准队友时叠加特殊准星 <0.不显示 1.仅使用默认准星时显示 3.一直显示>
cl_teamid_overhead_mode 2   		//隔墙显示队友位置	<0.不显示 1.透视队友位置 2.透视队友位置与装备>
cl_teammate_colors_show 1 		//竞技模式队友颜色	<0.不显示 1.显示颜色 2.显示颜色+英文首字母>
cl_hud_playercount_pos 0 		//比分,玩家信息位置  <0.顶部 1.底部>
cl_hud_playercount_showcount 0	//玩家信息显示样式 	<0.显示玩家头像 1.只显示数量>

r_drawtracers_firstperson 1   		//打开曳光弹道
r_dynamic 1   			//打开动态光	<0.关闭 牺牲光效略微提升fps>

gameinstructor_enable 0    		//关闭游戏教学
spec_replay_autostart 0    		//关闭被击杀回放
mm_dedicated_search_maxping 120    	//最大匹配延迟ms

ui_steam_overlay_notification_position "topright"  //steam提示出现位置 建议"bottomright" "topright"

//视频设置
mat_monitorgamma 1.8   		//亮度 越小越亮  	<1.6~2.6>
mat_monitorgamma_tv_enabled "0"  	//显示模式 	<1.电视 0.电脑屏幕>
mat_powersavingsmode "0"   		//关闭节能模式[不用改]
mat_queue_mode 2 			//多核CPU开启[不用改]

//声音设置
volume 				0.5 	//主音量（Sound volume）
snd_menumusic_volume   		0.3  	//主菜单音乐音量
snd_roundstart_volume 		0   	//回合开始音量
snd_roundend_volume 		0   	//回合结束音量
snd_mapobjective_volume 		0  	//炸弹/人质音量
snd_tensecondwarning_volume	 	0.3   	//十秒警告音量
snd_deathcamera_volume 		0  	//死亡视角音量
snd_mvp_volume 			0.3    	//MVP音量
snd_dzmusic_volume 		0.1  	//头号特训音量
snd_mute_losefocus	 		1	//后台播放声音=0，后台静音=1
voice_positional			0    	//关闭VOIP定位[不用改]
voice_modenable  			1    	//启用语音[不用改]
voice_enable   			1	//按键通话[不用改]

//HUD设置
cl_color 			3    	//队伍中颜色   	<0.黄色 1.紫色 2.绿色 3.蓝色 4.橙色>
cl_hud_color 		2    	//设置HUD颜色 	<0.默认 1.白色 2.淡蓝色 3.蓝色 4.紫色 5.红色 6.橙色 7.黄色 8.绿色 9.淡绿色 10.粉红色>
cl_hud_background_alpha 	0.5 	//HUD透明度	<0.5=50%>
cl_hud_healthammo_style  	0  	//生命值/弹药样式 	<0.默认 1.简约>
cl_hud_radar_scale 		1  	//雷达大小 	<0.8-1.3>
cl_radar_scale 		0.45  	//雷达缩放	
cl_radar_icon_scale_min 	0.6   	//雷达人物标点大小
cl_radar_rotate 		1  	//雷达旋转[不用改]
cl_radar_always_centered 	1  	//雷达以玩家为中心[不用改]
hud_showtargetid		1  	//显示队友/敌人id
hud_scaling  		0.85	//HUD缩放		<0.5~0.95> 默认0.85
safezonex 		1  	//HUD水平边缘距离
safezoney 		1    	//HUD竖直边缘距

//按键绑定
bind mouse4 "+voicerecord";		//前侧键使用麦克风

bind v +jumpthrow
bind space +jumpduck
alias +jumpthrow "+jump;-attack"
alias -jumpthrow -jump
alias +jumpduck "+jump;+duck"
alias -jumpduck "-jump;-duck"

bind mouse5 "toggle cl_righthand";		//切换左右手
bind alt noclip;
bind mwheelup +jump;
bind f "+lookatweapon"
alias +inspect "-lookatweapon; +reload"
alias -inspect "+lookatweapon; -reload"
bind c +cjump;		// 大跳
alias +cjump "+jump; +duck";
alias -cjump "-jump; -duck";
bind "w" "+forward; r_cleardecals"
bind "a" "+moveleft; r_cleardecals"
bind "d" "+moveright; r_cleardecals"
bind "s" "+back; r_cleardecals"
bind "mouse1" "+attack; r_cleardecals"

host_writeconfig;   //写入config,自动加载
echo "--- succesfully executed autoexec.cfg ---"

~~~

# S1mple准心
~~~
cl_crosshair_drawoutline "0"
cl_crosshair_dynamic_maxdist_splitratio "0.300000"
cl_crosshair_dynamic_splitalpha_innermod "1"
cl_crosshair_dynamic_splitalpha_outermod "0.5"
cl_crosshair_dynamic_splitdist "7"
cl_crosshair_friendly_warning "1"
cl_crosshair_outlinethickness "1"
cl_crosshair_sniper_show_normal_inaccuracy "0"
cl_crosshair_sniper_width "1"
cl_crosshair_t "0"
cl_crosshairalpha "255"
cl_crosshaircolor "4"
cl_crosshaircolor_b "255"
cl_crosshaircolor_g "0"
cl_crosshaircolor_r "1"
cl_crosshairdot "1"
cl_crosshairgap "-2.000000"
cl_crosshairgap_useweaponvalue "0"
cl_crosshairsize "1.000000"
cl_crosshairstyle "5"
cl_crosshairthickness "0"
cl_crosshairusealpha "1"
cl_fixedcrosshairgap "3"
cl_viewmodel_shift_left_amt "0.500000"
cl_viewmodel_shift_right_amt "0.250000"
viewmodel_fov "63"
viewmodel_offset_x "1.5"
viewmodel_offset_y "2"
viewmodel_offset_z "-2﻿"
viewmodel_presetpos "0"
viewmodel_recoil "0"
cl_bob_lower_amt "5.000000"
cl_bobamt_lat "0.100000"
cl_bobamt_vert "0.100000"
cl_bobcycle "0.98"
~~~

