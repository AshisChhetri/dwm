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
1. How to patch DWM.

    alwayscenter:
    [Always Center Patch:](https://dwm.suckless.org/patches/alwayscenter/)

    uselessgap:
    []()

    attachabove:
    []()

2. Create patche folder inside DWM Dir. you can undo changes..

    create and move patches inside <b>dwm/patches/</b>
    ```shell
    mkdir patches
    mv pathes/* /dwm/patches/
    ```
    To make backup
    ```shell
    cp config.h config.def.h
    ```
    To patch <b>DWM</b>
    ```shell
    # goto dwm folder.
    cd dwm
    
    #type patch -i patch_name
    patch -i patches/(patche name)

    # after patch make DWM again..
    sudo make clean install
    ```
    >[!NOTE] 
    > patching file does not make change in config.h
    > Cuz this is main config file..

    then restart dwm
    `Ctrl+Shift+q` exit <b>dwm</b>
    `xinitrc`

    

    
