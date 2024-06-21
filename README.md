# home-assistant-web3-build

This repository contains docker compose file with Home Assistant + ipfs daemon + libp2p proxy + zigbee2mqtt.

## Requirements 

Docker engine + docker compose.

**Docker should start without root preventives.** This is important to provide correct access to directories.

Install additional packages:
```commandline
sudo apt-get install wget unzip git jq
```

**Insert zigbee coordinator in your PC before start script!** 

## Configuration

First, download the repository and go to it:
```commandline
git clone https://github.com/airalab/home-assistant-web3-build
cd home-assistant-web3-build/
```

then you have to create `.env` file. Convert it from `template.env` file:
```commandline
cp template.env .env
```
After that,You may open the file and edit default values such as: 
- Versions of packages
- path to repository where will be stored all configurations folders.
- time zone in ["tz database name"](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones).



## Installation and Run

Run bash script:
```commandline
bash setup.sh
```

After everything started, Home Assistant web interface will be on 8123 port and zigbee2mqtt on 8099 port.


It will stop and delete running docker containers.

## Update 

To update version of packages, run `update.sh` script. It will stop running containers, dowload new version of packages and start everything again. This script will save all configurations files.


## Stop

To stop everything run stop script:
```commandline
bash stop.sh
```
