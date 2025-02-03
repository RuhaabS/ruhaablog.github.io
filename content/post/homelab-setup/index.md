---
title: Perfect Homelab Setup Guide 
date: 2025-01-24
description: Purpose of this guide is to setup my homelab exactly how I want it. 
tags: 
    - homelab
    - guide
---

# Overview

I will be using Kubernetes to host all my services and applications or maybe just docker containers depending on how well things work.

(This list is not complete and will likely be updated when I add more things)

The following services will be hosted:

1. Plex server
2. QBittorrent
3. Mincracft/Game servers
4. Auto free game redeem
5. Ollama to host AI LLM 
6. Dev server to code off IPad
7. PiHole for adfree YouTube on TV 
8. VPN to connect to back to machine from outside
9. Mylar comic book downloader
10. Some sort of network management
11. Maybe some sort of monitoring with Grafana

# Initial Setup

## Setup OS 

Install Ubuntu server edition by downloading from [here](https://ubuntu.com/download/server)

Flash a USB using [Rufus](https://rufus.ie/en/) and install on machine

## Setup SSH

Install OpenSSH server
```bash
sudo apt install openssh-server
```

Check Status
```bash
sudo systemctl status ssh
```
Enable SSH server
```bash
sudo systemctl enable ssh
```
Start SSH server
```bash
sudo systemctl start ssh
```
Allow SSH port 22 from firewall
```bash
sudo ufw allow ssh
sudo ufw enable
sudo ufw status
```
Should now be able to login
```bash
ssh {user}@{server_ip_host}
```

