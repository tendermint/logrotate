# docker-logrotate
Truncates container logs when they grow in size

Also rotate the tendermint consensus write-ahead-log (cswal).

## Usage

```
docker run -d --volumes-from <tmdata-container> -v /var/lib/docker/containers:/var/lib/docker/containers:rw tendermint/logrotate
```

where `<tmdata-container>` is the name of the tendermint data container (eg. `myapp_tmdata` if starting `myapp` via `mintnet`)


