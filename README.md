# Self Hosted Services 

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

## Requirments
* Docker
* docker-compose