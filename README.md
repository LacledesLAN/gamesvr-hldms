# Half-Life Deathmatch: Source Dedicated Server in Docker

Half-Life Deathmatch: Source is a Source engine port of the multiplayer portion of Half-Life. The game is given to players for free as part of their purchase of Half-Life: Source. Gameplay is similar to that of the original multiplayer component of Half-Life; players are spawned at random points across one of many maps and battle each other in an all out free-for-all.

![Half-Life Deathmatch: Source Screenshot](https://raw.githubusercontent.com/LacledesLAN/gamesvr-hldms/master/.misc/screenshot1.jpg "Half-Life Deathmatch: Source Screenshot")

This repository is maintained by [Laclede's LAN](https://lacledeslan.com). Its contents are intended to be bare-bones and used as a stock server. For examples of building a customized server from this Docker image browse its related child-project [gamesvr-hldms-freeplay](https://github.com/LacledesLAN/gamesvr-hldms-freeplay). If any documentation is unclear or it has any issues please see [CONTRIBUTING.md](./CONTRIBUTING.md).

## Linux

[![linux/amd64](https://github.com/LacledesLAN/gamesvr-hldms/actions/workflows/build-linux-image.yml/badge.svg)](https://github.com/LacledesLAN/gamesvr-hldms/actions/workflows/build-linux-image.yml)

### Download

```shell
docker pull lacledeslan/gamesvr-hldms;
```

### Run Self Tests

The image includes a test script that can be used to verify its contents. No changes or pull-requests will be accepted to this repository if any tests fail.

```shell
docker run -it --rm lacledeslan/gamesvr-hldms ./ll-tests/gamesvr-hldms.sh;
```

### Run Interactive Server

```shell
docker run -it --rm --net=host lacledeslan/gamesvr-hldms ./srcds_run -game hl1mp +map crossfire -maxplayers 8 +sv_lan 1;
```

## Getting Started with Game Servers in Docker

[Docker](https://docs.docker.com/) is an open-source project that bundles applications into lightweight, portable, self-sufficient containers. For a crash course on running Dockerized game servers check out [Using Docker for Game Servers](https://github.com/LacledesLAN/README.1ST/blob/master/GameServers/DockerAndGameServers.md). For tips, tricks, and recommended tools for working with Laclede's LAN Dockerized game server repos see the guide for [Working with our Game Server Repos](https://github.com/LacledesLAN/README.1ST/blob/master/GameServers/WorkingWithOurRepos.md). You can also browse all of our other Dockerized game servers: [Laclede's LAN Game Servers Directory](https://github.com/LacledesLAN/README.1ST/tree/master/GameServers).
