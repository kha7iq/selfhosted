# Self Hosted Services 

## Services 

[Adguard](/services/adguard.yml)

[Adminer](/services/adminer.yml)

[Bitwarde](/services/bitwarden.yml)

[Certdump](/services/certdumper.yml)

[Code Server](/services/code.yml)

[Drone-ci](/services/drone-ci.yml)

[Excalidraw](/services/excalidraw.yml)

[Searx](/services/find.yml)

[Gittea](/services/gittea.yml)

[Gotify](/services/gotify.yml)

[Guacamole](/services/guacamole.yml)

[Heimdall](/services/heimdall.yml)

[Jellyfin](/services/jellyfin.yml)

[Jenkins](/services/jenkins.yml)

[Mariadb](/services/mariadb.yml)

[Minio](/services/minio.yml)

[NextCloud](/services/nextcloud_nginx_default_backup)

[Plausible Analytics](/services/plausible-analytics.yml)

[Portainer](/services/portainer.yml)

[Postwomen](/services/postwomen.yml)

[Qbittorrent](/services/qbittorrent.yml)

[Redis](/services/redis.yml)

[Scrutiny](/services/scrutiny.yml)

[Authelia](/services/sso.yml)

[Synthing](/services/synthing.yml)

[Traefik 2](/services/traefik2.yml)

[Ubooquity](/services/ubooquity.yml)

[Whoogle](/services/whoogle.yml)

[Wikijs](/services/wikijs.yml)

[Youtube-dl](/services/youtube-dl.yml)


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