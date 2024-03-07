---
title: 設定「Xfce」搭配「Compiz」
nav_order: 7031
has_children: false
parent: 設定「Xfce」搭配其他的「視窗管理器」
grand_parent: 如何
---


# 設定「Xfce」搭配「Compiz」


## 微調腳本

| 微調腳本 |
| --- |
| [xfce-with-compiz](https://github.com/samwhelp/xubuntu-adjustment/tree/main/prototype/main/alternative-config/xfce-with-compiz/Main) |


## 前提

目前「Xubuntu」是採用「xfce」這個「桌面環境」，

搭配「xfwm4」這個「視窗管理器」。

現在我們要來嘗試讓「xfce」搭配「[compiz](https://samwhelp.github.io/note-about-xubuntu/read/master/window-manager/compiz.html)」。


## 操作步驟

* [安裝「Compiz」](#安裝compiz)
* [安裝「Compiz」設定檔](#安裝compiz設定檔)
* [設定「gtk-window-decorator」](#設定gtk-window-decorator)
* [設定「xfce-session」採用「compiz」](#設定xfce-session採用compiz)


## 安裝「Compiz」

執行下面指令，安裝「[compiz](https://packages.ubuntu.com/noble/compiz)」

``` sh
sudo apt-get install compiz
```

執行下面指令，安裝「[compizconfig-settings-manager](https://packages.ubuntu.com/noble/compizconfig-settings-manager)」

``` sh
sudo apt-get install compizconfig-settings-manager
```

執行下面指令，安裝「[compiz-plugins-main](https://packages.ubuntu.com/noble/compiz-plugins-main)」和「[compiz-plugins-extra](https://packages.ubuntu.com/noble/compiz-plugins-extra)」

``` sh
sudo apt-get install compiz-plugins-main compiz-plugins-extra
```

以上可以合併在一起，執行如下


``` sh
sudo apt-get install \
	compiz \
	compizconfig-settings-manager \
	compiz-plugins-main \
	compiz-plugins-extra

```


## 安裝「Compiz」設定檔

| 關於「Compiz」設定檔路徑 |
| --- |
| [~/.config/compiz-1/compizconfig/config](https://github.com/samwhelp/xubuntu-adjustment/blob/main/prototype/main/alternative-config/xfce-with-compiz/Main/asset/overlay/etc/skel/.config/compiz-1/compizconfig/config) |
| [~/.config/compiz-1/compizconfig/Default.ini](https://github.com/samwhelp/xubuntu-adjustment/blob/main/prototype/main/alternative-config/xfce-with-compiz/Main/asset/overlay/etc/skel/.config/compiz-1/compizconfig/Default.ini) |


``` sh
mkdir -p ~/.config/compiz-1/compizconfig

curl -fLo ~/.config/compiz-1/compizconfig/Default.ini --create-dirs https://raw.githubusercontent.com/samwhelp/xubuntu-adjustment/main/prototype/main/alternative-config/xfce-with-compiz/Main/asset/overlay/etc/skel/.config/compiz-1/compizconfig/Default.ini

curl -fLo ~/.config/compiz-1/compizconfig/config --create-dirs https://raw.githubusercontent.com/samwhelp/xubuntu-adjustment/main/prototype/main/alternative-config/xfce-with-compiz/Main/asset/overlay/etc/skel/.config/compiz-1/compizconfig/config

```


## 設定「gtk-window-decorator」

關於「compiz」預設採用的是「gtk-window-decorator」，

所以可以做如下的設定:

執行下面指令，設定視窗的標題列，顯示那些按鈕。

``` sh
gsettings set org.gnome.desktop.wm.preferences button-layout 'appmenu:minimize,maximize,close'
```

執行下面指令，安裝「numix-gtk-theme」

``` sh
sudo apt-get install numix-gtk-theme
```

執行下面指令，設定「gtk-window-decorator」採用「Numix」這個佈景主題。

``` sh
gsettings set org.gnome.desktop.wm.preferences theme 'Numix'
```


## 設定「xfce-session」採用「compiz」

| 設定檔路徑 |
| --- |
| [~/.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-session.xml](https://github.com/samwhelp/xubuntu-adjustment/blob/main/prototype/main/alternative-config/xfce-with-compiz/Main/asset/overlay/etc/skel/.config/xfce4/xfconf/xfce-perchannel-xml/xfce4-session.xml#L15) |


## 相關議題

| [佈景主題](https://samwhelp.github.io/note-about-xubuntu/read/subject/theme.html) |
| --- |
| [設定「Qt Style」](https://samwhelp.github.io/note-about-xubuntu/read/subject/theme/config/qt-style.html) |
