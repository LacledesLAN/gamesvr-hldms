# Half-Life Deathmatch: Source Dedicated Server in Docker

## Linux
[![](https://images.microbadger.com/badges/version/lacledeslan/gamesvr-hldms.svg)](https://microbadger.com/images/lacledeslan/gamesvr-hldms "Get your own version badge on microbadger.com")
[![](https://images.microbadger.com/badges/image/lacledeslan/gamesvr-hldms.svg)](https://microbadger.com/images/lacledeslan/gamesvr-hldms "Get your own image badge on microbadger.com")

**Download**
```
docker pull lacledeslan/gamesvr-hldms
```

**Run Interactive Server**
```
docker run -it --rm --net=host lacledeslan/gamesvr-hldms ./srcds_run -game hl1mp +map crossfire -insecure -maxplayers 8 -norestart +sv_lan 1
```

**Run Self Tests**
```
docker run -it --rm lacledeslan/gamesvr-hldms ./ll-tests/gamesvr-hldms.sh
```
