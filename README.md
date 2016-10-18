# MuslimLauncher开发文档

### 1.综述
2014年开始Android桌面Launcher开始流行起来了，跟原始的Android桌面相比，第三方推出的桌面Launcher软件操作轻便、界面简洁、功能丰富.迅速积累一定的用户量. 我们都知道桌面是手机的入口程序,,有一定量级用户的桌面应用就容易搭建自己的互联网生态圈，开发参照知名Launcher：Apus，Solo launcher。

### 2.Launcher功能规划

###### 2.1 Launcher基本功能

Luancher基本功能包括参照正常android手机，如排列所有App，添加widget，修改壁纸，拖动卸载应用，新建文件夹等

###### 2.2 Launcher扩展功能

除了实现基本的手机桌面功能，还需添加如下三个方面

	1.穆斯林工具：祷告详情，伊斯兰日历，附近清真，古兰经电台


	2.仿iOS功能：小白点assistive touch(辅助性工具 开关快捷健，一键清理)

	3.其他扩展：如天气,新闻热点,关于我们

###### 2.3 Launcher未完善功能
	1.推荐功能：目前推荐功能是随机推荐一款google play上的应用给用户，需完善的功能有服务端配置若干个应用，通过网格形式展示给用户。


	2.壁纸功能：壁纸根据表现分为静态壁纸和动态壁纸，根据来源分为本地壁纸和网络壁纸，需完善的功能有服务端配置阿语风格的静态壁纸和开发几款自己的动态壁纸动态壁纸（和普通apk一样）

	3.穆斯林工具：a，附近清真需标明清真饭店还是清真寺；b，古兰经电台需退后台还能播放
	
	4.其他功能：a，一些界面切换，展示需动画效果；b，桌面推荐搜索目前配在本地，需要配置在服务端并获取展示；

### 3.开发环境

	1.硬件：pc机，多部不同分辨率的android手机(阿语地区三星手机为主)

	2.软件：mac os 64位系统，eclipse或android studio开发工具

	3.语言：纯java

	4.兼容：应用兼容android4.0以上系统(4.0以下版本目前属于低端机,市场份额5%左右,因此不考虑)

### 4.项目说明

    1.项目地址:http://42.62.62.16/chendongdong/muslimlauncher   developer分支
    
    2.项目结构:基于android 4.0 Launcher基础上进行开发的，源码详见github,libraries存放引用的开源库,vitamio--流媒体播放，用于古兰经电台，SearchBox--全局搜索框框架，MaterialDesign--android 5.0的控件代码，google-play-services_lib--用于google play地图，即查找附近清真用到
    
    3.包名结构:packagename改为com.ilead.muslimlauncher，以前android4.0的源码分别放在com.android和com.ilead.launcher包下，org.arabeyes.itl为开源的穆斯林祷告计算和日历项目这些源码建议不要轻易修改，自己模块代码分别新建包放在com.ilead下
	
	4.代码结构:
			  com.ilead.common--通用代码块，各种util
			  com.ilead.assistivetouch--小白点
	          com.ilead.cleanmaster--一键清理
	          com.ilead.muslimtool--穆斯林工具
	          com.ilead.search--全局搜索
	          com.ilead.shortcut--快捷开关
	          com.ilead.wallpaper--壁纸
	          com.ilead.weather--天气
	          com.ilead.widget--widget插件
	          com.ilead.recommend--推荐应用
	          com.ilead.setting--桌面设置
		
	5.其他说明：语言分为英语（默认），中文，阿语 后续需要叫翻译人员翻译；资源图片目前只有一套，够用了，需要的话联系美术多出几套；注意测试有关google的服务时需要连vpn，android sdk选择 Google Apis 21.


### 5.总结
	开发时桌面功能参照 Apus开发，穆斯林功能参照IMuslim穆斯林助手,不清楚的地方参照注释和源码。附件是一些我以前下的参考项目，图片资源，项目文档，网页书签，或许对开发有帮助。
	
### 附.原型
![image](https://raw.githubusercontent.com/chendd/MuslimLauncher/master/%E9%A1%B9%E7%9B%AE%E5%8E%9F%E5%9E%8B/iLauncher_png/%E4%B8%BB%E7%95%8C%E9%9D%A2.png)

![image](https://raw.githubusercontent.com/chendd/MuslimLauncher/master/%E9%A1%B9%E7%9B%AE%E5%8E%9F%E5%9E%8B/iLauncher_png/%E5%85%A8%E5%B1%80%E6%90%9C%E7%B4%A2.png)

![image](https://raw.githubusercontent.com/chendd/MuslimLauncher/master/%E9%A1%B9%E7%9B%AE%E5%8E%9F%E5%9E%8B/iLauncher_png/%E6%82%AC%E6%B5%AE%E6%8C%89%E9%92%AE.png)

![image](https://github.com/chendd/MuslimLauncher/blob/master/%E9%A1%B9%E7%9B%AE%E5%8E%9F%E5%9E%8B/iLauncher_png/%E8%8F%9C%E5%8D%95%E8%AE%BE%E7%BD%AE.png?raw=true)
    
