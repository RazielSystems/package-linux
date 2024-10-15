# Archivos de configuración e instalación de Linux (ArchLinux - Manjaro)


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
