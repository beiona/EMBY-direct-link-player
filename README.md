# EMBY-direct-link-player
# 感谢各位mjj对本项目的支持与帮助
老项目：https://github.com/beiona/emby-goindex-potplayer

本次更新，新版本EMBY 4.6.7.0可用
https://github.com/MediaBrowser/Emby.Releases/releases/tag/4.6.7.0

# 特点
1. Rclone挂载网盘作为EMBY的片源仓库。
2. 2. 同一个网盘搭建了列表程序（goindex，oneindex，onemanager）。 
3. 3. 播放时不走服务器流量，播放网盘直链。

# 效果
EMBY和Goindex挂载同一个谷歌网盘，目录结构基本一样。
替换emby视频路径，直接调用potplayer播放网盘内的视频。

按按钮调用potplayer，播放网盘直链

<img width="658" alt="image" src="https://raw.githubusercontent.com/beiona/emby-goindex-potplayer/main/%E6%B2%B9%E7%8C%B4%E8%84%9A%E6%9C%AC/emby-goindex-potplayer01.PNG">

<img width="658" alt="image" src="https://raw.githubusercontent.com/beiona/emby-goindex-potplayer/main/%E6%B2%B9%E7%8C%B4%E8%84%9A%E6%9C%AC/emby-goindex-potplayer02.PNG">


# 使用方法
<img width="658" alt="image" src="https://raw.githubusercontent.com/beiona/EMBY-direct-link-player/main/pic01.PNG">
把jquery-3.6.0.min.js和mjj.js两个文件放入/opt/emby-server/system/dashboard-ui/文件夹


<img width="658" alt="image" src="https://raw.githubusercontent.com/beiona/EMBY-direct-link-player/main/pic02.PNG">
修改同目录下index.html文件，在body里加两行
<script type="text/javascript" src="./jquery-3.6.0.min.js"></script>
<script type="text/javascript" src="./mjj.js"></script>


<img width="658" alt="image" src="https://raw.githubusercontent.com/beiona/EMBY-direct-link-player/main/pic03.PNG">
修改mjj.js文件，共三处。
第一处16行
第二处18行
第三处21-24行，四选一

# 举例
<img width="658" alt="image" src="https://raw.githubusercontent.com/beiona/EMBY-direct-link-player/main/pic04.PNG">
Rclone的挂载目录


<img width="658" alt="image" src="https://raw.githubusercontent.com/beiona/EMBY-direct-link-player/main/pic05.PNG">
网盘的列表程序目录


<img width="658" alt="image" src="https://raw.githubusercontent.com/beiona/EMBY-direct-link-player/main/pic06.PNG">
把不同的前缀填入mjj.js即可

# 可能遇到的问题
replace()指令不生效

你的浏览器可能不支持该js指令，具体见

https://caniuse.com/?search=replace%20string
