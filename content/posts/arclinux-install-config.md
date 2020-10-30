#### icon

```shell
yay -S moka-icon-theme-git
```



#### 输入法框架fcitx5

```shell
# 安装fcitx5
sudo pacman -S fcitx5-im
# 配置fcitx5支持
vim ~/.pam_environment

INPUT_METHOD DEFAULT=fcitx5
GTK_IM_MODULE DEFAULT=fcitx5
QT_IM_MOUDLE DEFAULT=fcitx5
XMODIFIERS DEFAULT=\@im=fcitx5

# 中文输入引擎
sudo pacman -S fcitx5-chinese-addons
#  UI库和支持
sudo pacman -S fcitx5-qt
sudo pacman -S fcitx5-gtk
sudo pacman -S fcitx5-qt4-git
# fcitx5配置工具
sudo pacman -S fcitx5-configtool
# zhwiki和萌娘百科词库
sudo pacman -S fcitx5-pinyin-zhwiki fcitx5-pinyin-moegirl
# 皮肤
sudo pacman -S fcitx5-material-color
```



#### mplayer

```shell
sudo pacman -S mplayer
```





#### visual studio code

```shell
sudo pacman -S visual-studio-code-bin
```



#### sublime

```shell
# 配置sublime服务器地址
curl -O https://download.sublimetext.com/sublimehq-pub.gpg && sudo pacman-key --add sublimehq-pub.gpg && sudo pacman-key --lsign-key 8A8F901A && rm sublimehq-pub.gpg
   82  echo -e "\n[sublime-text]\nServer = https://download.sublimetext.com/arch/stable/x86_64" | sudo tee -a /etc/pacman.conf
# 安装
sudo pacman -S sublime-text
```



#### tmux

```shell
sudo pacman -S tmux
```



#### calibre(kindle)

```shell
sudo pacman -S calibre
```



#### typora(Markdown编辑器)

```shell
sudo pacman -S typora
```



#### v2ray

```shell
sudo pacman -S v2ray
```



#### v2ray client

```shell
# 选择安装qv2ray
# pacman -S v2ray-desktop
# 客户端需要v2ray-core 首先需要安装v2ray
yay -S qv2ray 
```

#### 微信

```shell
yay -S deepin-wine-wechat
```

#### wps办公软件

```shell
yay -S wps-office
```

#### plank(docker)

```shell
sudo pacman -S plank

## aur theme
yay -S plank-theme-arc
yay -S plank-theme-namor
yay -S plank-theme-numix
```



#### hugo(blog引擎)

```shell
sudo pacman -S hugo
```

#### Android Studio

##### https://wiki.archlinux.org/index.php/Android_(%E7%AE%80%E4%BD%93%E4%B8%AD%E6%96%87)

```shell
# 先安装sdk
yay -S android-sdk
yay -S android-sdk-platform-tools
yay -S android-sdk-build-tools
# 安装sdk平台软件包
yay -S android-platform-21

# 安装android-studio
sudo pacman -S android-studio

```



### pacman

```shell
# 更新系统
sudo pacman -Syyu

# 递归删除孤立软件包
pacman -Rns $(pacman -Qtdq)
-Qt : 仅显示真的孤立包，要包含可选依赖，使用-Qtt
```

