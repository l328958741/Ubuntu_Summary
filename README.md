# Ubuntu_Summary
记录，总结使用ubuntu系统遇到的各种问题

# 安装环境介绍
--------------------
* 虚拟机：VMware® Workstation 14 Pro；版本：14.1.1 build-7528167
* 主机操作系统：Windows 10, 64-bit  (Build 17134) 10.0.17134
* 安装的Ubuntu 16.04 LTS，内存2G，2核，64位，硬盘空间100G
* 学习内容：用于学习nodeJS，运行Ebookchain，部署服务器

# 遇到的问题
---------------------
* 下载各种软件速度过慢
    * 安装完ubuntu后，直接更换下载源（用阿里云的源）
    * [配置方法]https://blog.csdn.net/sikong00/article/details/80237415
    * sudo apt-get update(更新源列表)， sudo apt upgrade（更新软件）
* 屏幕过小--xrandr -s 1600x1200
* root权限管理
    * 设置root权限密码：sudo passwd
    * 进入root账户：su
* 安装nvm，node的版本管理器
    * [参考文档]https://www.jianshu.com/p/8671e439a811
    * 配置淘宝源--在终端输入>ls -a查看文件，直接进入home文件夹下，
按住ctrl+h可以打开隐藏文件，找到.bashrc文件，右键“open with gedit”， 按住ctrl+f，调出查找框，
找到nvm，“export NVM_DIR="/home/lzc/.nvm"
export NVM_NODEJS_ORG_MIRROR=https://npm.taobao.org/mirrors/node//在两句之间输入这个代码
[ -s "$NVM_DIR/nvm.sh" ] && . "$NVM_DIR/nvm.sh"  # This loads nvm”，即可配置完成，
关闭终端，再次打开可以使用nvm install 8.6.0，速度特别快
    * 安装node的版本为8.6.0，运行ebookchain的需要
* 中文输入法修改--[参考文档]https://www.cnblogs.com/darklights/p/7722861.html
* 安装IDE--[安装vscode]https://www.jianshu.com/p/7038e201bf36，指令sudo dpkg -i <filename>.deb
* git配置ssh密钥
    * >ssh-keygen ；>cd /home/ann/.ssh/；>ls -a；>cat id_rsa.pub
    * 复制公钥，在git账号上注册，进入setting 进入ssh and Gpg keys，输入公钥
