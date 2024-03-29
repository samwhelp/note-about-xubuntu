---
title: 設定「Xfce」搭配「Bspwm」
nav_order: 7052
has_children: false
parent: 設定「Xfce」搭配其他的「視窗管理器」
grand_parent: 如何
---


# 設定「Xfce」搭配「Bspwm」


## 微調腳本

| 微調腳本 |
| --- |
| [xfce-with-bspwm](https://github.com/samwhelp/xubuntu-adjustment/tree/main/prototype/main/alternative-config/xfce-with-bspwm/Main) |


## 前提

目前「Xubuntu」是採用「xfce」這個「桌面環境」，

搭配「xfwm4」這個「視窗管理器」。

現在我們要來嘗試讓「xfce」搭配「[bspwm](https://samwhelp.github.io/note-about-xubuntu/read/master/window-manager/bspwm.html)」。


## 操作步驟

* [安裝「Bspwm」](#安裝bspwm)
* [關於「Bspwm」設定檔](#關於bspwm設定檔)
* [設定「xfce-session」採用「bspwm」](#設定xfce-session採用bspwm)


## 安裝「Bspwm」

執行下面指令，安裝「[bspwm](https://packages.ubuntu.com/noble/bspwm)」和「[sxhkd](https://packages.ubuntu.com/noble/sxhkd)」

``` sh
sudo apt-get install bspwm sxhkd
```


## 關於「Bspwm」設定檔

| 關於「Bspwm」設定檔路徑 |
| --- |
| [~/.config/bspwm/bspwmrc](https://github.com/samwhelp/xubuntu-adjustment/blob/main/prototype/main/alternative-config/xfce-with-bspwm/Main/asset/overlay/etc/skel/.config/bspwm/bspwmrc) |
| [~/.config/bspwm/sxhkdrc](https://github.com/samwhelp/xubuntu-adjustment/blob/main/prototype/main/alternative-config/xfce-with-bspwm/Main/asset/overlay/etc/skel/.config/bspwm/sxhkdrc) |


## 設定「xfce-session」採用「bspwm」

| 設定檔路徑 |
| --- |
| [~/.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-session.xml](https://github.com/samwhelp/xubuntu-adjustment/blob/main/prototype/main/alternative-config/xfce-with-bspwm/Main/asset/overlay/etc/skel/.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-session.xml#L15) |
