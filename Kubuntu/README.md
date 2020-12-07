# Kubuntu
Start from a clean Kubuntu 20.10 installation, I did this

## System Update and Additional Drivers
- **Update**: `sudo apt update && sudo apt dist-upgrade -y`
- **Additional Drivers**: `sudo apt install kubuntu-driver-manager`

## Look
- **Konsole Profile**: https://store.kde.org/p/1322967 (you can install it using the Konsole profile settings)
- **Desktop 1 Wallpaper**: https://www.wallpaperflare.com/digital-digital-art-artwork-fantasy-art-drawing-painting-wallpaper-gjwku
- **Desktop 2 Wallpaper**: https://www.wallpaperflare.com/digital-digital-art-artwork-kvacm-fantasy-art-knight-silhouette-wallpaper-udeev (for two screens setup)
- **Spectrum Charoite Global Theme**: https://store.kde.org/p/1449948
- **Sweet Aurorae Window Decorations**: https://store.kde.org/p/1286856

You will get something like this

![Inserire Link Screen 1]()

![Inserire Link Screen 2]()

## Installed Software

### Settings and Tweaks
- **Slimbook Battery**: 
	- Add repository: `sudo add-apt-repository ppa:slimbook/slimbook`
	- Update: `sudo apt update`
	- Install: `sudo apt install slimbookbattery -y`
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
- **IPython**: `sudo apt install ipython3 -y`
- **Maven**: `sudo apt install maven -y`
- **Postman**: `sudo snap install postman`

You can find some useful conda command in the *conda-help* file

### Tools
- **OBS-Studio**: `sudo snap install obs-studio`
- **Stacer**: `sudo apt install stacer -y`
- **SendAnywhere**:
	- Download: https://send-anywhere.com/file-transfer
	- Execute .deb file to install (e.g. using `dpkg` or the snap store)
- **htop**: `sudo apt install htop -y`

### Office
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
- **Mailspring**: 
  - Install Keyring Dependency: `sudo apt install gnome-keyring -y`
  - Install: `sudo snap install mailspring`
- **Skype**: `sudo snap install skype --classic`
- **Zoom**: `sudo snap install zoom-client`
- **Telegram**: `sudo apt  install telegram-desktop -y`

## To Install
- Angular
- Docker + Docker Compose
- JupyterLab
- Virtualbox
