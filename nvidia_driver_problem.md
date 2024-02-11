# 现象
ubuntu20.04黑屏系统进不去,光标闪烁
![picture](https://picx.zhimg.com/70/v2-8e031442fc8b1cd8fcfe18fc28aec9a7_1440w.avis?source=172ae18b&biz_tag=Post)

# 问题原因
系统升级导致的显卡驱动出现了问题。

# 解决方法
1.终端输入：

ubuntu-drivers devices

查看自己的是否是nvidia的显卡驱动，最后有个recommended的就是推荐的安装

2.如果安装推荐版本直接：

sudo ubuntu-drivers autoinstall

无需进行任何设置 ，安装完成后sudo reboot

3.重启后，输入这个查看是否安装成功了

nvidia-smi

