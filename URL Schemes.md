# Usage of URL Schemes for Inter-App Communication

## Objective-C

        \#define iOS10 ([[UIDevice currentDevice].systemVersion doubleValue] >= 10.0)
        NSString * urlString = @"App-Prefs:root=WIFI";
        if ([[UIApplication sharedApplication] canOpenURL:[NSURL URLWithString:urlString]]) {
            if (iOS10) {
                [[UIApplication sharedApplication] openURL:[NSURL URLWithString:urlString] options:@{} completionHandler:nil];
            } else {
                [[UIApplication sharedApplication] openURL:[NSURL URLWithString:urlString]];
            }
        }

## Swift

        if let url = URL(string:"App-Prefs:root=WIFI") {
            if #available(iOS 10.0, *) {
                UIApplication.shared.open(url, options: [:], completionHandler: nil)
            } else {
                UIApplication.shared.openURL(url)
            }
        }

# List of URL Schemes for Inter-App Communication

## Before iOS10

        蜂窝网络：prefs:root=MOBILE_DATA_SETTINGS_ID
        — prefs:root=General&path=Network/
        Wi-Fi：prefs:root=WIFI
        定位服务：prefs:root=LOCATION_SERVICES
        个人热点：prefs:root=INTERNET_TETHERING
        关于本机：prefs:root=General&path=About
        辅助功能：prefs:root=General&path=ACCESSIBILITY
        飞行模式：prefs:root=AIRPLANE_MODE
        锁定：prefs:root=General&path=AUTOLOCK
        亮度：prefs:root=Brightness
        蓝牙：prefs:root=Bluetooth
        时间设置：prefs:root=General&path=DATE_AND_TIME
        FaceTime：prefs:root=FACETIME
        设置：prefs:root=General
        设置 prefs:root=SETTING
        定位服务 prefs:root=LOCATION_SERVICES
        键盘设置：prefs:root=General&path=Keyboard
        iCloud：prefs:root=CASTLE
        iCloud备份：prefs:root=CASTLE&path=STORAGE_AND_BACKUP
        语言：prefs:root=General&path=INTERNATIONAL
        定位：prefs:root=LOCATION_SERVICES
        音乐：prefs:root=MUSIC
        Music Equalizer — prefs:root=MUSIC&path=EQ
        Music Volume Limit — prefs:root=MUSIC&path=VolumeLimit
        Network — prefs:root=General&path=Network
        Nike + iPod — prefs:root=NIKE_PLUS_IPOD
        Notes — prefs:root=NOTES
        Notification — prefs:root=NOTIFICATIONS_ID
        Phone — prefs:root=Phone
        Photos — prefs:root=Photos
        Profile — prefs:root=General&path=ManagedConfigurationList
        Reset — prefs:root=General&path=Reset
        Safari — prefs:root=Safari
        Siri — prefs:root=General&path=Assistant
        Sounds — prefs:root=Sounds
        Software Update — prefs:root=General&path=SOFTWARE_UPDATE_LINK
        Store — prefs:root=STORE
        Twitter — prefs:root=TWITTER
        Usage — prefs:root=General&path=USAGE
        Wallpaper — prefs:root=Wallpaper

        电话 mobilephone://
        备忘录 mobilenotes://
        墨客 com.moke.moke-1://
        名片全能王 camcard://
        扫描全能王 camscanner://
        TuneIn Radio tunein:// 或 tuneinpro://
        OfficeSuite mobisystemsofficesuite://
        WPS Office KingsoftOfficeApp://
        Line line://
        1Password onepassword://
        Clear(著名的Todo应用) clearapp://
        Chrome谷歌浏览器 googlechrome://
        Calendars 5 calendars://
        GoodReader 4 com.goodreader.sendtogr://
        PDF Expert 5 pdfexpert5presence://
        Documents 5 rdocs://
        nPlayer nplayer-http://
        GPlayer gplayer://
        AVPlayer HD AVPlayerHD://
        AVPlayer AVPlayer://
        Ace Player aceplayer://
        12306订票助手 trainassist://
        金山词霸 com.kingsoft.powerword.6://
        节奏大师 tencentrm://
        赶集生活 **://
        凤凰新闻 comIfeng3GifengNews://
        高铁管家 gtgj://
        飞信 fetion://
        豆瓣FM doubanradio://
        大智慧 dzhiphone://
        布卡漫画 buka://
        爱奇艺PPS ppstream://
        哔哩哔哩动画 bilibili://
        56视频 com.56Video://
        365日历 rili365://
        58同城 wbmain://
        遇见 iaround://
        陌陌 momochat://
        有道词典 yddict://
        优酷 youku://
        掌阅iReader iReader://
        艺龙旅行 elongIPhone://
        迅雷+迅雷云播 thunder://
        熊猫公交 wb1405365637://
        携程无线 CtripWireless://
        无线苏州 SuZhouTV://
        唯品会 vipshop://
        微视 weishiiosscheme://
        微拍 wpweipai://
        旺信 wangxin://
        网易公开课 ntesopen://
        网易将军令 netease-mkey://
        万年历 youloft.419805549://
        土豆视频 tudou://
        同花顺 amihexin://
        天涯社区 tianya://
        天气通Pro sinaweatherpro://
        天气通 sinaweather://
        墨迹天气 rm434209233MojiWeather://
        淘宝旅行 taobaotravel://
        人人 renrenios://
        蜻蜓FM qtfmp://
        浦发银行 wx1cb534bb13ba3dbd://
        招商银行 cmbmobilebank://
        建设银行 wx2654d9155d70a468://
        工商银行 com.icbc.iphoneclient://
        酷我音乐 com.kuwo.kwmusic.kwmusicForKwsing://
        酷狗音乐 kugouURL://
        今日头条 snssdk141://
        京东 openApp.jdMobile://
        QQ mqq://
        微信 wechat:// 或 weixin://
        QQ音乐 qqmusic://
        QQ斗地主 tencent382://
        QQ浏览器 mttbrowser://
        QQ安全中心 qmtoken://
        QQ国际版 mqqiapi://
        腾讯新闻 qqnews://
        腾讯微云 weiyun://
        腾讯地图 sosomap://
        腾讯企业邮箱 qqbizmailDistribute2://
        腾讯手机管家 mqqsecure://
        腾讯视频 tenvideo:// 或 tenvideo2:// 或 tenvideo3://
        腾讯微博 TencentWeibo://
        天天星连萌 tencent100689806://
        天天爱消除 tencent100689805://
        天天酷跑 tencent100692648://
        天天飞车 tencent100695850://
        PPTV pptv://
        爱奇艺视频 qiyi-iphone://
        暴风影音 com.baofeng.play://
        保卫萝卜2 wb2217954495://
        保卫萝卜 wb1308702128://
        百度音乐 baidumusic://
        百度视频 baiduvideoiphone:// 或 bdviphapp://
        百度糯米 bainuo://
        百度魔图 photowonder://
        百度魔拍 wondercamera://
        百度地图 baidumap://
        百度导航 bdNavi://
        百度 baiduboxapp:// 或 BaiduSSO://
        搜狗输入法 com.sogou.sogouinput://
        搜狐视频 sohuvideo-iphone:// 或 sohuvideo://
        搜狐新闻 sohunews://
        随手记 FDMoney://
        天天动听 ttpod://
        挖财记账 wacai://
        威锋网 com.weiphone.forum://
        新浪微博 weibo:// 或 sinaweibo://
        网易邮箱 neteasemail://
        高德导航 Autonavi://
        百度输入法 BaiduIMShop://
        百度贴吧 com.baidu.tieba://
        淘宝 taobao://
        天猫 tmall://
        支付宝 alipay://
        旺旺卖家版 wangwangseller://
        百度云 baiduyun://
        网易新闻 newsapp://
        UC浏览器 ucbrowser://
        E-Mail MESSAGE://


## After iOS10

        无线局域网	App-Prefs:root=WIFI
        蓝牙	App-Prefs:root=Bluetooth
        蜂窝移动网络	App-Prefs:root=MOBILE_DATA_SETTINGS_ID
        个人热点	App-Prefs:root=INTERNET_TETHERING
        运营商	App-Prefs:root=Carrier
        通知	App-Prefs:root=NOTIFICATIONS_ID
        通用	App-Prefs:root=General
        通用-关于本机	App-Prefs:root=General&path=About
        通用-键盘	App-Prefs:root=General&path=Keyboard
        通用-辅助功能	App-Prefs:root=General&path=ACCESSIBILITY
        通用-语言与地区	App-Prefs:root=General&path=INTERNATIONAL
        通用-还原	App-Prefs:root=Reset
        定位设置 App-Prefs:root=Privacy&path=LOCATION
        墙纸	App-Prefs:root=Wallpaper
        Siri	App-Prefs:root=SIRI
        隐私	App-Prefs:root=Privacy
        Safari	App-Prefs:root=SAFARI
        音乐	App-Prefs:root=MUSIC
        音乐-均衡器	App-Prefs:root=MUSIC&path=com.apple.Music:EQ
        照片与相机	App-Prefs:root=Photos
        FaceTime	App-Prefs:root=FACETIME
        电池电量 App-Prefs:root=BATTERY_USAGE
        存储空间 App-Prefs:root=General&path=STORAGE_ICLOUD_USAGE/DEVICE_STORAGE
        显示设置 App-Prefs:root=DISPLAY
        声音设置 App-Prefs:root=Sounds
        App Store 设置 App-Prefs:root=STORE
        打开电话 App-Mobilephone://
        世界时钟 App-Clock-worldclock://
        闹钟 App-Clock-alarm://
        秒表 App-Clock-stopwatch://
        倒计时 App-Clock-timer://
        打开相册 App-Photos://
