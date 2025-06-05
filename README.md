# Изменить горячие клавиши для раскдладки
```bash
# Изменить
gsettings set org.gnome.desktop.wm.keybindings switch-input-source "['<Alt>Shift_L', '<Alt>Shift_R', '<Shift>Alt_L', '<Shift>Alt_R']"
# Посмотреть
gsettings get org.gnome.desktop.wm.keybindings switch-input-source
```
# Скачать двайвера для принтера
```bash
sudo apt install printer-driver-gutenprint -y
```
# Настройка GIT
```bash
git config --global user.email "kologermit@gmail.com"
git config --global user.name kologermit
```
# Установка всех необходимых программ
```bash
sudo apt update
sudo apt upgdare -y
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
  outline-client \
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
  steam \
  printer-driver-gutenprint
```
# Настройка горячих клавиш
```bash
# Открытие терминала на Super+R
gsettings set org.gnome.settings-daemon.plugins.media-keys custom-keybindings "['/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/']"
gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/ name "Terminal"\ngsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/ command "gnome-terminal"\ngsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/ binding "<Super>r"

# Открытие проводника на Super+E
gsettings set org.gnome.settings-daemon.plugins.media-keys custom-keybindings \\n"['/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom0/', \\n '/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom1/']"
gsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom1/ name "Files"\ngsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom1/ command "nautilus --new-window"\ngsettings set org.gnome.settings-daemon.plugins.media-keys.custom-keybinding:/org/gnome/settings-daemon/plugins/media-keys/custom-keybindings/custom1/ binding "<Super>e"
```

# Убрать иконки с рабочего стола
```bash
dconf write /org/gnome/desktop/background/show-desktop-icons false
```
