# Archivos de configuración e instalación de Linux (ArchLinux - Manjaro)

# Configuración inicial

```bash
sudo pamac build mkinitcpio-firmware
sudo pacman -Syyu
sudo pamac update --no-confirm
sudo pamac checkupdates -a | awk '{print $1" "}'
```

## docker 
#### IP range 

```bash
sudo mkdir /etc/docker
vim /etc/docker/daemon.json

sudo pamac install --no-confirm docker docker-compose docker-scan
sudo systemctl enable --now docker
sudo usermod -aG docker $USER
```

[daemon.js](etc/docker/daemon.json)


## impresoras
```bash
sudo pamac install --no-confirm manjaro-printer system-config-printer simple-scan
sudo systemctl enable --now cups
```
