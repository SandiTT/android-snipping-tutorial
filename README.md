# android-snipping-tutorial

Packet capture depend on magisk、lsposed



# 必须先安装magisk和lsposed
# 必须有root权限，免root的不适用于这个教程





1、解压 HttpCanary高级版  

    1）手机打开设置搜索证书，安装CA证书，找到解压缩目录的HttpCanary.pem，安装完成   
    2）将HttpCanary.pem重命名为HttpCanary.jks
    3）使用MT管理器将HttpCanary.jks复制到/data/data/com.guoshi.httpcanary/cache/，如果失败说明没有root权限，用magisk授予root权限即可  
    4）安装HttpCanary.apk到手机
2、安装TrustMeAlready-v1.11-release.apk
    1) 安装完成后，打开lsposed，模块中找到TrustMeAlready
    2) 勾选HttpCanary和需要抓包的软件
3、（重启）非必须
4、打开HttpCanary
    1）左侧菜单栏进入设置
    2）找到抓包设置---->HttpCanary根证书
    3）如果上面的步骤没有问题，那么应该会显示已安装
    PS：也可以通过下方的**添加根证书到系统**移动个人证书到系统中，没试过
5、返回主页，左侧菜单栏进入目标应用
    PS：目标应用需要和上面TrustMeAlready设置的生效应用一致
6、回到主页开启抓包
7、启动需要抓包的应用



# ELM抓包

+ 不使用TrustMeAlready是无法成功截取全部的请求的，该软件用了证书绑定
+ 获取elm token只需要过滤url链接：h5.ele.me，然后选择请求，将cookie复制到剪切板即可，虽然软件中通过key:value显示，但是剪切板里的格式和网页请求里的cookie一样

# TO BE CONTINUED
