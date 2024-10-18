# DWM install and Setup

Install <b>yay</b>.. in <b>/opt</b> Dir
 ```shell
    sudo pacman -S --needed git base-devel
    cd /opt
    sudo git clone https://aur.archlinux.org/yay.git
    sudo chown -R $(whoami):$(whoami) yay
    cd yay
    makepkg -si
```
---
1. Clone <b>DWM</b>, <b>dmenu</b> & <b>st</b>
    
    Clone <b>DWM</b> git repo..
    ```shell
    git clone https://git.suckless.org/dwm
    ```
    Clone <b>dmenu</b> repo
    ```shell
    git clone https://git.suckless.org/dmenu
    ```
    Clone <b>st</b> repo..
    ```shell
    git clone https://git.suckless.org/st
    ```
2. Copy file in Suckless folder& install dwm, dmenu & st.

    move file to suckless dir. 
    ```shell
    mkdir suckless
    mv dwn dmenu st suckless/
    ```
    Install DWM
    ```shell
    cd suckless/dwm
    sudo make clean install
    ```
    Install dmenu
    ```shell
    cd ../dmenu
    sudo make clean install
    ```
    Install st
    ```shell
    cd ../st
    sudo make clean install
    ```

---
## set resolution
check monitor Spec
```shell
xrandr
```
Set resolution
```shell
xrandr --output "{monitor}" --mode "1920x1080"
```
# KeyBinds

|`|

| Key | feature |
| --- | --- |
|`Alt + Shift + Return`| Open <b>st</b> termianl|       
|`Alt + j`|select Forward window |
|`Alt + k`|select Backward Window |
|`Alt + h`|select | 
|`Alt + l`|select |
|`Shift + c`|Close window |       
|`Alt + p`|Open <b>dmenu</b> | 
|`Alt + Shift + {workspace no.}`|Move Window to WorkSpace.|
|`Alt + f`| floating Window mode. |

   
# DWM patching
1. Center floating window.

    [Always Center](https://dwm.suckless.org/patches/alwayscenter/)
    

    
