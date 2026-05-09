# Fast deploy rust desk private server

# 1. Start Service

```shell
docker-compose up -d
```

# 2. Get Key
```text
root@js:/usr/local/infra/desk# docker-compose logs -f 
hbbr  | [2026-05-09 02:45:22.324546 +00:00] INFO [src/relay_server.rs:61] #blacklist(blacklist.txt): 0
hbbr  | [2026-05-09 02:45:22.324568 +00:00] INFO [src/relay_server.rs:76] #blocklist(blocklist.txt): 0
hbbr  | [2026-05-09 02:45:22.324572 +00:00] INFO [src/relay_server.rs:82] Listening on tcp :21117
hbbr  | [2026-05-09 02:45:22.324574 +00:00] INFO [src/relay_server.rs:84] Listening on websocket :21119
hbbr  | [2026-05-09 02:45:22.324582 +00:00] INFO [src/relay_server.rs:87] Start
hbbr  | [2026-05-09 02:45:22.324655 +00:00] INFO [src/relay_server.rs:105] DOWNGRADE_THRESHOLD: 0.66
hbbr  | [2026-05-09 02:45:22.324695 +00:00] INFO [src/relay_server.rs:115] DOWNGRADE_START_CHECK: 1800s
hbbr  | [2026-05-09 02:45:22.324700 +00:00] INFO [src/relay_server.rs:125] LIMIT_SPEED: 32Mb/s
hbbr  | [2026-05-09 02:45:22.324703 +00:00] INFO [src/relay_server.rs:136] TOTAL_BANDWIDTH: 1024Mb/s
hbbr  | [2026-05-09 02:45:22.324706 +00:00] INFO [src/relay_server.rs:146] SINGLE_BANDWIDTH: 128Mb/s
hbbs  | [2026-05-09 02:45:22.441009 +00:00] INFO [src/common.rs:147] Private/public key written to id_ed25519/id_ed25519.pub
### hbbs  | [2026-05-09 02:45:22.441042 +00:00] INFO [src/rendezvous_server.rs:1251] Key: wV5THLnUXnWtxIiqkB0wctu+ritPpuGQk3pycKVgQR8=
hbbs  | [2026-05-09 02:45:22.441058 +00:00] INFO [src/peer.rs:84] DB_URL=./db_v2.sqlite3
hbbs  | [2026-05-09 02:45:22.445066 +00:00] INFO [src/rendezvous_server.rs:107] serial=0
hbbs  | [2026-05-09 02:45:22.445074 +00:00] INFO [src/common.rs:45] rendezvous-servers=[]
hbbs  | [2026-05-09 02:45:22.445077 +00:00] INFO [src/rendezvous_server.rs:109] Listening on tcp/udp :21116
hbbs  | [2026-05-09 02:45:22.445079 +00:00] INFO [src/rendezvous_server.rs:110] Listening on tcp :21115, extra port for NAT test
hbbs  | [2026-05-09 02:45:22.445081 +00:00] INFO [src/rendezvous_server.rs:111] Listening on websocket :21118
hbbs  | [2026-05-09 02:45:22.445136 +00:00] INFO [src/rendezvous_server.rs:146] mask: None
hbbs  | [2026-05-09 02:45:22.445141 +00:00] INFO [src/rendezvous_server.rs:147] local-ip: ""
hbbs  | [2026-05-09 02:45:22.445152 +00:00] INFO [src/common.rs:45] relay-servers=[]
hbbs  | [2026-05-09 02:45:22.445197 +00:00] INFO [src/rendezvous_server.rs:161] ALWAYS_USE_RELAY=N
hbbs  | [2026-05-09 02:45:22.445207 +00:00] INFO [src/rendezvous_server.rs:193] Start
hbbs  | [2026-05-09 02:45:22.483156 +00:00] INFO [libs/hbb_common/src/config.rs:895] Generated new keypair for id: 
```

# 3. Config Client

```text

ID Server: Your Server IP:21116

Relay Server: Your Server IP:21117

API Server: just let it blank

Key: wV5THLnUXnWtxIiqkB0wctu+ritPpuGQk3pycKVgQR8=

```

# 4. done
