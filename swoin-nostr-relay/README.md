# How to install a swoin nostr relay

This document describes the installation process of a swoin compatible nostr relay with HTTPS support.

## precondition

Linux Server + Docker

## Prepare files

copy _docker-compose.yml_ to your server in a subfolder of your choice

edit and copy in the same subfolder following files (keep folder structure):

- _caddy/Caddyfile_ (contains the domaininfos)
- _data/relay/config.toml_ (contains configuration for nostr)

## create Volume to store nostr database files

```bash
docker volume create nostrvol
```

## start all

```bash
docker compose up -d
```

## Add relay to swoin

use the second domain from your Caddyfile to add your relay to swoin
