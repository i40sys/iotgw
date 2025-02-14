# IoT Gateway NG

Woking on opening an internal project to the public.

## Video Demo

- Networking overview (Zerotier + bridged network)
- Povisioning: How to deploy base image (netboot) + Base system (af)
- Centralized and automated management: Ansible + Ansible Forms
- Backup image and restore (netboot)
- Rescue processes (netboot live image + ssh)
- Basic system management (OpenWRT UI + ttyd + ssh)
- Stacks: containers management (Docker + GitOps + Dockge)
- Observability: Grafana Alloy + Global Grafana (logs and metrics, supported OTel)
- Monitoring: Uptime Kuma + Global Grafana
- Backup: Duplicati + Telegraf + InfluxDB + Grafana
- MQTT: Mosquitto + EMQX
- Automation: Node-RED (Git based flows)
- Development: VSCode in-browser
- Documentation: Notion + Git hooks
- Development base image: Ansible creation base image

## Features

- iPXE based installation (netboot using HTTP and clonezilla)
- Centralized deployment (Ansible Forms + GitOps)
- GIT + configuration management (Notion configs as CMDB) - Ansible Forms link and Ansible forms JSON config file
- Applications with web interfaces for managementps
  - Dockge, container management
  - GLPI agent, inventory
  - Grafana Alloy, agent for observability and centralized logs
  - Uptime Kuma (Kuma + Autokuma), monitoring integrated with observability
  - Zerotier, VPN
  - Duplicati, backup
    - uses Telegraf for getting telemetry and injecting it into InfluxDB
  - Mosquitto, MQTT broker bidirectional integration with central EMQX
  - Node-RED, IoT automation and data flows. Git based stack and Git based config and flows
  - VSCode, in-browser development
- Applications documentation synchoronized with Notion (README.md -> Notion using GIT hooks)
- Grafana dashboards for monitoring and centralized alarms
  - [Monitoring dashboards (Grafana MIMIR)](https://grafana.com/grafana/dashboards/22535-system-and-containers-monitoring/)
  - Centralized logs (Grafana LOKI) - system and container logs
  - Backup status
  - Centralized alarms
- Web based system management (OpenWRT based)
  - Docker containers
  - Firewall and NAT
  - System processes
  - Real Time graphs of system resources
  - NTP server and client
  - DNS server and forwarder
  - DHCP server and client
  - Package manager
  - Startup services
  - Cron jobs

## Users

- System Administrators are the users of this project
- Developers/Contributors are the ones that evolve the project

## Brainstorming

- squashfs github workflow
- wireguard
- [grub-brts](https://github.com/Antynea/grub-btrfs) -> recuperar snapshots fallados de sistema
- Set-up public netboot
- Cronicle (central crontab management)
- Web terminal
- Composecraft
- Coolify, Dokploy, Convex, or similar for central deployment
- Kestra, or similar for central automation

## Reference

### Related projects

- https://meta-os.eu/

### Uptime Kuma

- https://github.com/louislam/uptime-kuma
- https://github.com/louislam/uptime-kuma/wiki
- https://github.com/BigBoot/AutoKuma/tree/master
- https://github.com/lucasheld/uptime-kuma-api
- https://uptime-kuma-api.readthedocs.io/en/latest/
- https://github.com/carlbomsdata/uptime-kuma-agent
- https://github.com/jmclaren7/uptime-kuma-push
- https://blog.programster.org/uptime-kuma-configure-push-monitor
