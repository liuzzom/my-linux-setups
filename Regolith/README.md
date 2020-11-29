# My Regolith configuration

## System Update and Regolith Installation

### System Update
Starting from a clean Ubuntu 20.04 LTS installation, you have to:
- Update your system, using the System Update utility or using the following command:
`sudo apt update && sudo apt dist-upgrade -y`
### Install Regolith:
- Add Regolith release PPA: `sudo add-apt-repository ppa:regolith-linux/release`
- Install Regolith: `sudo apt install regolith-desktop-mobile`
- Close the current session (or reboot the system) and select "Regolith" during login

After login, you will see something like this

![Screen 01](https://github.com/liuzzom/my-linux-setups/blob/main/Regolith/img/screen_01.png)

A *Remontoire* screen will explain you some basics keybindings (e.g. open a terminal, launch rofi menu, open nautilus, etc). You can open/close this window using `<Super>+<Shift>+<?>`

## Regolith Customization
### Theme
- Install Ubuntu Regolith theme: `sudo apt install regolith-look-ubuntu` (another cool theme is `regolith-look-pop-os`)
- The Wallpaper can be changed using the gnome settings
- You can change the Regolith theme in two ways:
	- by using the traditional CLI command: `regolith-look set <name>`
	- by using a GUI selector: `<Super>+<Alt>+<L>`

If you changed the theme using the CLI command, you have to restart i3 with `<Super>+<Shift>+<R>` and refresh regolith-looks using `regolith-look refresh`

### Bar Indicators:
- Search available indicators: `apt search ^i3xrocks-`
- Install some indicator: `sudo apt install <indicator-name>` 
- In my installation:
	- I installed *volume*, *wifi* and the *todo* indicators:
	  `sudo apt install i3xrocks-volume i3xrocks-wifi i3xrocks-todo`
- After you installed or removed some i3xrocks packages, you have to restart i3 using `<Super>+<Shift>+<R>`
### Look
Most of the changes are made by modifyng the *~/.Xresources-regolith*, some are made by using *gnome-tweaks*. 

Terminal color schemes are installed using *Gogh* (I use the *Foxnightly* profile with some tweaks ). 

I used `rofi-theme-selector` to select the *Purple* theme.

- **Fonts**:
	- Download *JetBrains* font from here: https://www.jetbrains.com/lp/mono/
	- Download *Menlo for Powerline*: https://github.com/abertsch/Menlo-for-Powerline
	- Create the *~/.fonts* directory
	- Unzip and copy all *.ttf* file in the *~/.fonts* directory
	- Some changes are made using tweaks (All fonts are setted to *Ubuntu Medium 11*)
- **GTK Theme**: *gnome.gtk.theme: Yaru-dark* entry in `~/.XResources-regolith` file
- **GTK Icon Theme**: *gnome.icon.theme: Yaru-dark* entry in `~/.XResources-regolith` file
- **Rofi Icon Theme**: *rofi.icon.theme: Yaru-dark* entry in `~/.XResources-regolith` file
- **i3 Borders**: see *Borders* section in `~/.XResources-regolith`

After all Tweaks, you will obtain something like this:

![Screen 02](https://github.com/liuzzom/my-linux-setups/blob/main/Regolith/img/screen_02.jpg)

## Installed Softwares
### Settings and Tweaks
- **Gnome-Tweaks**: `sudo apt install gnome-tweaks`
	
	- Using Gnome Tweaks you can change GTK Themes, GTK Icons, Shell Theme and more, but I suggest you to do it by modifing the `.Xresources-Regolith` file
- **Slimbook Battery**: 
	- Add repository: `sudo add-apt-repository ppa:slimbook/slimbook`
	- Update: `sudo apt update`
	- Install: `sudo apt install slimbookbattery -y`
- **Alacarte**: `sudo apt install alacarte -y`
- **Gogh**:
	- Install Dependencies: `sudo apt-get install dconf-cli uuid-runtime`
	- Run in the interactive mode: `bash -c  "$(wget -qO- https://git.io/vQgMr)"`
- **Powerline-Shell**
	
	- Add repository: `sudo add-apt-repository universe`
	- Install: `sudo apt install --yes powerline`
	- Add the following lines to your $HOME/.bashrc file:
	```bash
	# Powerline configuration
	if [ -f /usr/share/powerline/bindings/bash/powerline.sh ]; then
	  powerline-daemon -q
	  POWERLINE_BASH_CONTINUATION=1
	  POWERLINE_BASH_SELECT=1
	  source /usr/share/powerline/bindings/bash/powerline.sh
	fi
	```
	- Use `source ~/.bashrc` to apply changes

### Developing Tools
- **VS Code**: 
	- Download: https://code.visualstudio.com/docs/?dv=linux64_deb
	- Execute *.deb* file to install (e.g. using `dpkg` or the snap store)
	- Set Menlo font for the terminal: https://dev.to/mattstratton/making-powerline-work-in-visual-studio-code-terminal-1m7
- **Git**: `sudo apt install git`
- **JetBrains**: 
	- Download: https://www.jetbrains.com/toolbox-app/
	- Unzip the archive
	- Run the installer (either from CLI or clicking on its icon)
- **OpenJDK 11**: `sudo apt install openjdk-11-jdk`
- **Sublime Text**: `sudo snap install sublime-text  --classic`
- **Eclipse**:
	- Download: https://www.eclipse.org/downloads/download.php?file=/oomph/epp/2020-09/R/eclipse-inst-jre-linux64.tar.gz
	- Unzip the archive
	- Run the installer
- **NodeJS**: `sudo apt install nodejs -y`
- **NPM**: `sudo apt install npm -y`
- **Miniconda**: 
	- Download: https://docs.conda.io/en/latest/miniconda.html
	- Run the installer: `bash Miniconda3-latest-Linux-x86_64.sh` (you don't need to use `sudo`)
- **IPython**: `sudo apt install ipyhton3`
- **Maven**: `sudo apt install maven`

You can find some useful conda command in the conda-help file
### Tools
- **OBS-Studio**: `sudo snap install obs-studio`
- **Stacer**: `sudo apt install stacer`
- **SendAnywhere**:
	- Download: https://send-anywhere.com/file-transfer
	- Execute .deb file to install (e.g. using `dpkg` or the snap store)
- **htop**: `sudo apt install htop`

### Office
- **Okular**: `sudo snap install okular`
- **Joplin**: `sudo snap install joplin-james-carroll`
- **OnlyOffice**: `sudo snap install onlyoffice-desktopeditors`
- **Typora**:
	- `wget -qO - https://typora.io/linux/public-key.asc | sudo apt-key add -`
	- `sudo add-apt-repository 'deb https://typora.io/linux ./'`
	- `sudo apt-get update`
	- `sudo apt-get install typora -y`

### Media
- **VLC**: `sudo apt install vlc`

### Web
- **Chrome**:
	- Download: https://www.google.it/chrome/index.html
	- Execute *.deb* file to install (e.g. using `dpkg` or the snap store)
- **Brave**:
	- `sudo apt install apt-transport-https curl gnupg`
	- `curl -s https://brave-browser-apt-release.s3.brave.com/brave-core.asc | sudo apt-key --keyring /etc/apt/trusted.gpg.d/brave-browser-release.gpg add -`
	- `echo "deb [arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main" | sudo tee /etc/apt/sources.list.d/brave-browser-release.list`
	- `sudo apt update`
	- `sudo apt install brave-browser`
- **Mailspring**: `sudo snap install mailspring`
- **Skype**: `sudo snap install skype --classic`
- **Zoom**: `sudo snap install zoom-client`

## Useful References
- **Regolith Installation**: https://regolith-linux.org/docs/getting-started/install/
- **Regolith Basic Usage**: https://regolith-linux.org/docs/getting-started/basics/
- **Regolith Look**: https://regolith-linux.org/docs/customize/look/
- **Regolith How-To**: https://regolith-linux.org/docs/howto/
- **Install Font**: https://www.getdroidtips.com/install-fonts-ubuntu/
- If You have some trouble with **Gogh**: https://github.com/Mayccoll/Gogh/issues/177

## To Install
- Angular
- Docker + Docker Compose
- JupyterLab
- Postman
- Virtualbox

## To Do
- Create a BASH script to download and install everything
