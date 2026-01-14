# Reset password admin
```
[root@tele script]# docker ps
CONTAINER ID   IMAGE                                  COMMAND                  CREATED        STATUS        PORTS                                       NAMES
62171ee4ddfd   alert-idc                              "/bin/sh -c 'pip ins…"   7 months ago   Up 2 months                                               alert-idc
420c0a30f140   prom/prometheus:latest                 "/bin/prometheus --c…"   2 years ago    Up 2 months   0.0.0.0:9090->9090/tcp, :::9090->9090/tcp   prometheus
f83c9359a47d   grafana/grafana-image-renderer:3.5.0   "dumb-init -- node b…"   2 years ago    Up 2 months   127.0.0.1:8083->8081/tcp                    grafana-renderer-1
98d76f3fe5aa   grafana/grafana:8.1.8                  "/run.sh"                2 years ago    Up 2 months   0.0.0.0:3000->3000/tcp, :::3000->3000/tcp   grafana-grafana-1
[root@tele script]# docker exec -u root -it 98d76f3fe5aa grafana-cli admin reset-admin-password L!fFc6lkC6B^PY
-bash: !fFc6lkC6B^PY: event not found
[root@tele script]# docker exec -u root -it 98d76f3fe5aa grafana-cli admin reset-admin-password 'L!fFc6lkC6B^PY'
INFO[01-14|03:29:57] Connecting to DB                         logger=sqlstore dbtype=sqlite3
INFO[01-14|03:29:57] Starting DB migrations                   logger=migrator
INFO[01-14|03:29:57] migrations completed                     logger=migrator performed=0 skipped=330 duration=1.382163ms

Admin password changed successfully ✔
```
