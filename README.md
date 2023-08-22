# Self Hosted Services 

## Services 


### A
[Adguard](/services/adguard.yml)

[Adminer](/services/adminer.yml)

[Authelia](/services/sso.yml)


### C
[Certdump](/services/certdumper.yml)

[Code Server](/services/code.yml)

[CrowdSec](/services/crowdsec.yml)

### D
[Drone-ci](/services/drone-ci.yml)

### E
[Excalidraw](/services/excalidraw.yml)

### F
[File Browser](services/filebrowser.yml)

### G
[Ghost Blog](services/ghost-blog.yml)

[Gitea](/services/gitea.yml)

[Gotify](/services/gotify.yml)

[Guacamole](/services/guacamole.yml)

### H
[Heimdall](/services/heimdall.yml)

### J
[Jellyfin](/services/jellyfin.yml)

[Jenkins](/services/jenkins.yml)

### M
[Mariadb](/services/mariadb.yml)

[Minio](/services/minio.yml)

### N
[Net Data](services/netdata.yml)

[Navidrome](services/navidrome.yml)

[NextCloud](/services/nextcloud.yml)

### P
[Pi-Hole](services/pihole.yml)

[Plausible Analytics](/services/plausible-analytics.yml)

[Portainer](/services/portainer.yml)

[Postwomen](/services/postwomen.yml)

[PyLoad](services/pyload.yml)

### Q
[Qbittorrent](/services/qbittorrent.yml)

### R
[Redis](/services/redis.yml)

### S
[Searx](/services/find.yml)

[Scrutiny](/services/scrutiny.yml)

[Syncthing](/services/synthing.yml)

### T
[Traefik 2](/services/traefik2.yml)

### U
[Ubooquity](/services/ubooquity.yml)

### V
[Vault Warden](/services/vaultwarden.yml)

### W
[Whoogle](/services/whoogle.yml)

[Wikijs](/services/wikijs.yml)

[Wireguard](/services/wireguard.yml)

### Y
[Youtube-dl](/services/youtube-dl.yml)

### Gitlab in Kubernetes
[Gitlab Kubernetes](https://github.com/kha7iq/gitlab-k8s)

## How to use this repo:

Clone the repo using:

```
$ git clone https://github.com/m47ik/selfhosted.git $HOME/selfhosted
```


## Traefik Network

Create the **home_net** network with:

```
$ docker network create -d macvlan --subnet=192.168.0.0/24 --gateway=192.168.0.1 -o parent=eth0 home_net
```

I use this method so that I can assign static IPs to containers. You can set the subnet and gateway as per your network.

Also this is not compulsory, you can create the `home_net` as docker network and us internal ips. Simply remove the following part from docker-compose manifests.
```yaml
    networks:
      home_net:
        ipv4_address: 192.168.xx.xx
```

## Requirements
* Docker
* docker-compose
