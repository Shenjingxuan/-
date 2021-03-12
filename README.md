# -
微信小游戏反编译教程

一，安装夜神模拟器

模拟器用于在pc上运行微信
安装完成后，搜索微信并安装
（自行搜索下载）

二，下载RE管理器

RE管理器用于访问文件夹
安装后打开时，提示超级用户权限，点击允许,会提示获取超管权限点击同意
(该安装包已在本分支中文件后缀名为.apk)

三，模拟器运行小游戏

打开微信，并搜索小游戏打开
运行小游戏时，小游戏的包会保存在/data/data/com.tencent.mm/MicroMsg/{{一串32位的16进制字符串名文件夹}}/appbrand/pkg/目录下

四，导出小游戏包

在/data/data/com.tencent.mm/MicroMsg/{{一串32位的16进制字符串名文件夹}}/appbrand/pkg/目录下根据时间找到小游戏包wxapkg
长按wxapkg文件，点击右上角3个点，选择压缩文件
点击查看
跳转到zip包所在文件夹，然后长按文件，选择右上角，并选择发送
选择发送给朋友（微信分身的文件传输工具)，这样就可以在pc端微信接收这个文件，并保存到桌面

五，反编译

安装nodejs，下载地址：http://nodejs.cn/
下载反编译脚本，（已在本分支中 为zip格式压缩包）解压后在此文件夹内执行命令行操作
安装完nodejs后，在下载的反编译脚本文件夹里，shift+鼠标右键，打开命令窗口
npm install esprima
npm install css-tree
npm install cssbeautify
npm install vm2
npm install uglify-es
npm install js-beautify
npm install escodegen
安装以上完毕后，开始反编译wxappg文件（在当前目录下）
输入： node wuWxapkg.js D:\wxappg\haidao.wxapkg\haidao.wxapkg（后边微信小游戏包换成实际所在位置） 
而后同一级目录下会出现一个同名的文件夹
