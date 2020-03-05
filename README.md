# 华为光猫破解教程
## 前言
### 破解光猫必备要求
- 有原光猫超密（最好要有，方便获取宽带信息）  
- 有宽带的loid（部分需要password）  
- 有宽带账号密码  
- 记下宽带的Vlan ID  
- 
##### 在此diss【宽带论坛】【恩山无线】  
两大坑害换光猫用户的论坛  
各种资源全部被这两大论坛封锁，用户上传的固件教程被这些论坛管理员删除，拿去售卖  
把其他用户摸索出来后分享的教程，转身删除，拿去咸鱼售卖  
你们这些不要脸的，我在这里要“亲切”问候你  
你们要脸吗？不！你们没有脸！  
你们只想着赚用户的钱，甚至还在论坛发着错误教程让别人变砖，还口口声声的在论坛说帮别人修砖不值得，不“浪费时间”  
现实是你们咸鱼的交易量可观，这就是你们口中的“不浪费时间”修砖，真可谓是滑天下之大稽  
#### 注意事项
##### 本教程以及其包含的固件、工具所有人可免费下载，完全开源，开源协议遵照“[CC-BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh)”，
![image](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)
##### 其意思为“知识共享-署名-非商业性-相同方式共享，即此教程共享，转发必须注明作者本人-不允许以各种方法拿此教程获利，此共享协议对中国大陆有效，用本教程获利的人，我将保留依法追责的权力！

#### 本教程适用于华为光猫的破解，主要内容包括：
- [开启telnet](#开启telnet)
- [补全shell](#补全shell)
- [修改连接设备数量](#修改连接设备数量)
- [修改到原厂界面](#修改到原厂界面)
- [修改到电信界面](#修改到电信界面)
- [修改到联通界面](#修改到联通界面)
- [修改到移动界面](#修改到移动界面)
- [itms伪认证](#itms伪认证)
- [改E/G模式（部分可改双模）](#改E/G模式)  
- [救砖方法](#救砖方法)
- [相应工具的分享](#相应工具的分享)
## 正文
### 开启telnet
telnet，乃破解光猫必有的一项，开启后可通过telnet对光猫进行修改，如获取超密、修改界面、更改光模块运行模式等等。  
开启此模式前，请确保你的电脑开启了telnet功能，具体方法请自行百度。  
早期光猫可以使用“组播工具”使能方式开启光猫的telnet功能，随着华为升级光猫固件，这种方法在新光猫上已经失效，现给出目前已知的2种开启方案  
##### 1· 使用超密开启  
使用超密登录光猫后，进入“安全>ONT访问控制配置”，将“使能LAN侧PC通过TELNET访问设备”勾选，即可开启telnet（如下图）其他界面开启方式大同小异  
![image](https://github.com/2879597772/ONT/blob/master/images/open_telnet.jpg)
##### 2· 修改配置开启
部分光猫由于地区/固件影响，没有办法用上图方式开启telnet，但若在“管理>设备管理”中有“USB备份设置”的话，即可用此方法开启telnet  
·在“USB备份设置”中勾选“快速恢复”以便恢复配置  
·在光猫背面插入U盘后点击“备份配置”（插入U盘后刷新界面） 

![image](https://github.com/2879597772/ONT/blob/master/images/open_telnet2.jpg)  
· 拔出U盘，插入电脑，可以看见U盘目录下有“e8_Config_Backup”文件夹，内有一个*.cfg的文件，此文件就是我们要修改的文件  
· 此文件一般都被加密，请使用目录工具中的“华为配置文件解密工具”进行解密  
· 将配置文件“<X_HW_CLITelnetAccess”字段做如下修改： 
```   
<X_HW_CLITelnetAccess Access="1" TelnetPort="23" OutTelnetPort="23"/>  
```
· 加密后插会光猫，将光猫断电重启，配置文件即可恢复
### 补全shell
### 修改连接设备数量
### 修改到原厂界面
### 修改到电信界面
### 修改到联通界面
### 修改到移动界面
### itms伪认证
### 改E/G模式
### 救砖方法
### 相应工具的分享

有时间再慢慢写，感兴趣就fork此项目哦