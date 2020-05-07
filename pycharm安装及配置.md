pycharm版本：pycharm-community-2018.3.7，之后的不支持32位系统，[官网下载链接](https://www.jetbrains.com/pycharm/download/other.html)，默认安装。

启动 pycharm 弹出“Failed to load JVM.... DLL\bin\server\jvm.dll”错误，参考[此解决方法](https://blog.csdn.net/knight_zhou/article/details/103739864)后判断是缺少jdk。

按照[JDK下载安装及环境变量配置的图文教程（详解）](https://blog.csdn.net/konggu_youlan/article/details/79942800)，[Oracle官网下载](https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html)适用于32位系统、Windows7的jdk-8u251-windows-i586并安装配置。
安装路径为默认的C:\Program Files\Java\jdk1.8.0_251\，其中jre安装时要求空文件夹，故在此路径下新建jdkjre，但安装完后此路径下自动生成了jre文件夹，所以环境变量还是与教程一样。此外与教程完全相同。
