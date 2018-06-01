Listen 1 音乐播放器（桌面版）
=========================

Listen 1可以搜索和播放来自网易云音乐，虾米，QQ音乐三个主流音乐网站的歌曲，让你的曲库更全面。并支持收藏功能，方便的创建自己的歌单。

[![imgur](http://i.imgur.com/Ae6ItmA.png)]()

* 支持Windows，Mac，Linux平台


生成完整代码方法一（适用于fork后从自己的git下拉取）
-----------
项目中包含了listen1_chrome_extension的引用，在checkout后需要把引用库初始化

    要把listen1大佬的.gitmodules文件里的url换成了https://github.com/listen1/listen1_chrome_extension.git,然后执行下面的命令没问题
    git submodule update --init --recursive
    

生成完整代码方法二（适用于直接从listen1下拉取）
-----------
项目中包含了listen1_chrome_extension的引用，在checkout后需要把引用库初始化
   
    删除.gitmodules文件、app/listen1_chrome_extension目录
    git rm -rf --cached app/listen1_chrome_extension  
    git submodule add https://github.com/listen1/listen1_chrome_extension.git  app/listen1_chrome_extension（重新生成.gitmodules文件）

运行
----

    npm run start

生成安装包
---------
全平台安装包

    npm run dist

Windows安装包

    npm run dist:win32
    npm run dist:win64
    
Mac安装包

    npm run dist:mac
    
Linux安装包

    npm run dist:linux32
    npm run dist:linux64
