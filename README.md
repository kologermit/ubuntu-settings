# Комбинации клавиш
```bash
# Изменить
gsettings set org.gnome.desktop.wm.keybindings switch-input-source "['<Alt>Shift_L', '<Alt>Shift_R', '<Shift>Alt_L', '<Shift>Alt_R']"
# Super+E для открытия проводника (Files)
gsettings set org.gnome.settings-daemon.plugins.media-keys custom-keybindings "['/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/']"
gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/ name "Open Files"
gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/ command "nautilus"
gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/ binding "<Super>e"
# Super+R для открытия терминала
gsettings set org.gnome.settings-daemon.plugins.media-keys custom-keybindings "['/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom1/']"
gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom1/ name "Open Terminal"
gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom1/ command "gnome-terminal"
gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom1/ binding "<Super>r"
# Alt+F5 для выключения системы
gsettings set org.gnome.settings-daemon.plugins.media-keys custom-keybindings "['/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom1/', '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom2/']"
gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom2/ name "Shutdown"
gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom2/ command "gnome-session-quit --power-off"
gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom2/ binding "<Alt>F5"
```
# Установка всех необходимых программ
```bash
sudo apt update
sudo apt upgdare -y
wget -qO- https://us-apt.pkg.dev/doc/repo-signing-key.gpg | sudo gpg --dearmor -o /etc/apt/trusted.gpg.d/gcloud-artifact-registry-us.gpg
echo "deb [arch=amd64] https://us-apt.pkg.dev/projects/jigsaw-outline-apps outline-client main" | sudo tee /etc/apt/sources.list.d/outline-client.list
wget -O- https://download.docker.com/linux/ubuntu/gpg | gpg --dearmor | sudo tee /etc/apt/keyrings/docker.gpg > /dev/null && echo "deb [arch=amd64 signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu noble stable"| sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt update
apt-cache policy docker-ce
sudo apt install -y \
  micro \
  wireguard \
  curl \
  wget \
  python3-venv \
  vim \
  git \
  kolourpaint \
  chrome-gnome-shell \
  gcc \
  g++ \
  cmake \
  make \
  python3-pip \
  mysql-client \
  postgresql-client \
  gnome-terminal \
  zsh \
  gamemode \
  tar \
  printer-driver-gutenprint \
  software-properties-common \
  ca-certificates \
  apt-transport-https \
  nano \
  docker-ce \
  docker-compose \
  openssh-server \
  vlc \
  tldr \
  ntfs-3g
sudo snap install mattermost-desktop
sudo snap install obsidian --classic
mkdir -p ~/Downloads
cd ~/Downloads
wget "https://cloudcdn-mar-57.cdn.yandex.net/download.cdn.yandex.net/browser/yandex/25_4_1_1132_80909/Yandex.deb"
sudo apt install ./Yandex.deb -y
sudo systemctl enable docker
sudo usermod -aG docker $USER
newgrp docker
docker ps
```
# Настройка GIT
```bash
git config --global user.email "kologermit@gmail.com"
git config --global user.name kologermit
```
# Настройка рабочего стола
```bash
dconf write /org/gnome/desktop/background/show-desktop-icons false
gsettings set org.gnome.shell.extensions.ding show-home false
gsettings set org.gnome.shell.extensions.ding show-trash false
gsettings set org.gnome.shell.extensions.dash-to-dock dock-position 'BOTTOM'
gsettings set org.gnome.desktop.background picture-uri "file://$HOME/desktop.jpg"
gsettings set org.gnome.desktop.background picture-uri-dark "file://$HOME/desktop.jpg"
```
