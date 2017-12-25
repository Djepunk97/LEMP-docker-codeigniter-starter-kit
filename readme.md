# LEMP docker starter integrated with Codeigniter

Quick learning, deubgging, playing with [Codeigniter](https://codeigniter.com/) just one line of command.

# Prerequisite

Windows requires 64bit Windows 10 Pro with Hyper-V available. Please see What to know before you install for a full list of prerequisites.

macOS & Others unix just download and install on docker official site.

# Usage

## Create and Start Containers

```
$ docker-compose up -d
```

If you already ```docker-compose up -d``` you can just

```
$ docker-compose start
```

## Stop Containers

```
$ docker-compose stop
```

## Stop and remove containers, networks, images, and volumes

```
$ docker-compose down
```

---

# Structures

## Overall structures

```
├── docker-compose.yml
├── mysql
│   └── conf
├── nginx
│   ├── conf
│   ├── log
│   └── site
└── phpfpm
    └── conf
        ├── cli
        └── fpm
```
## Private IP Address

Private address which container talk to each others
(If you want to access with host just add uncomment in docker-compose.yml)

```
Gateway: 172.20.1.1
Subnet: 172.20.0.0/16

Nginx: 172.20.1.2
PhpFPM: 172.20.1.3
MySQL: 172.20.1.4
```
