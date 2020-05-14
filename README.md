# rollenspielsache-meta

This repository contains planning and cross-component configurations that don't belong to a specific repo.

## Component List

### Library

* [librollenspielsache](https://github.com/deciduously/librollenspielsache) - Rust core library.  C-compatible.  [crates.io](https://crates.io/crates/librollenspielsachedocr) - [docs.rs](https://docs.rs/librollenspielsache/0.1.2/rollenspielsache/index.html)
* [librollenspielsache-rb](https://github.com/deciduously/librollenspielsache-rb) - Ruby bindings for `librollenspielsache`. [rubygems.org](https://rubygems.org/gems/librollenspielsache-rb)

### Clients

* [rollenspielsache-svc](https://github.com/deciduously/rollenspielsache-svc) - REST/GraphQL API
* [rollenspielsache-www](https://github.com/deciduously/rollenspielsache-www) - Frontend web application
* [rollenspielsache-bot](https://github.com/deciduously/rollenspielsache-bot) - Discord bot

## Deployment

Currently `rollenspielsache-svc` is deployed at `rollenspielsache.deciduously.com`, using NGINX as a reverse proxy to `localhost:9292`, where the Docker container is mounted.  I have the main page on `localhost:8080`.  Only 443/SSL connections are accepted, see `nginx/sites-available` for configuration blocks.  The host is a DigitalOcean droplet running Ubuntu 20.04, with `docker`, `ufw`, `nginx`.