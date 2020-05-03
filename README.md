# traefik-plex-rr
docker compose for a traefik proxy'd plex, sonarr radarr and such
## 1 Update and install curl
```apt update && sudo aptt upgrade -y && sudo apt install curl -y```
## 2 Install rclone and configure your drive
## 3 edit crontab and add : 
```@reboot rclone mount --config=PATH/TO/rclone.conf --allow-other --allow-non-empty --fast-list --drive-skip-gdocs --vfs-read-chunk-size=64M --vfs-read-chunk-size-limit=2048M --buffer-size=64M --poll-interval=1m --dir-cache-time=168h --timeout=10m --drive-chunk-size=64M --umask=002 --syslog -v DRIVE-NAME: /data/drive```
## 4 install docker
```curl https://get.docker.com/ | sudo bash```
## 5 copy treafik.yml to /opt/traefik
## 6 docker-compose.yml
```docker-compose up -d```
## Enjoy!
