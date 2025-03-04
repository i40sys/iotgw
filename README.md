# IoT Gateway NG

Woking on opening an internal project to the public.

## Video Demo

- Networking overview (Zerotier + bridged network)

[![Networking overview](https://img.youtube.com/vi/6T7rvnrf6K4/0.jpg)](https://www.youtube.com/embed/6T7rvnrf6K4?si=U8OCnHJ-6hS1b_Uk)

- Povisioning: How to deploy base image (netboot) + Base system (af)

[![Povisioning: How to deploy base image (netboot) + Base system (af)](https://img.youtube.com/vi/aq3I2qahD7U/0.jpg)](https://www.youtube.com/embed/aq3I2qahD7U?si=U8OCnHJ-6hS1b_Uk)

- Centralized and automated management: Ansible + Ansible Forms

[![Centralized and automated management: Ansible + Ansible Forms](https://img.youtube.com/vi/nD3MafF8zLU/0.jpg)](https://www.youtube.com/embed/nD3MafF8zLU?si=U8OCnHJ-6hS1b_Uk)

- Backup image and restore (netboot)

[![Backup image and restore (netboot)](https://img.youtube.com/vi/Jz8XUtylkBI/0.jpg)](https://www.youtube.com/embed/Jz8XUtylkBI?si=U8OCnHJ-6hS1b_Uk)

- Rescue processes (netboot live image + ssh)

[![Rescue processes (netboot live image + ssh)](https://img.youtube.com/vi/XLT-ElDg0NM/0.jpg)](https://www.youtube.com/embed/XLT-ElDg0NM?si=U8OCnHJ-6hS1b_Uk)

- Basic system management (OpenWRT UI + ttyd + ssh)

[![Basic system management (OpenWRT UI + ttyd + ssh)](https://img.youtube.com/vi/e-h6pZ5Qd1U/0.jpg)](https://www.youtube.com/embed/e-h6pZ5Qd1U?si=U8OCnHJ-6hS1b_Uk)

- Stacks: containers management (Docker + GitOps + Dockge)

[![Stacks: containers management (Docker + GitOps + Dockge)](https://img.youtube.com/vi/kQc9rAQwNEE/0.jpg)](https://www.youtube.com/embed/kQc9rAQwNEE?si=U8OCnHJ-6hS1b_Uk)

- Observability: Grafana Alloy + Global Grafana (logs and metrics, supported OTel)

[![Observability: Grafana Alloy + Global Grafana (logs and metrics, supported OTel)](https://img.youtube.com/vi/44clHt8Mp8M/0.jpg)](https://www.youtube.com/embed/44clHt8Mp8M?si=U8OCnHJ-6hS1b_Uk)

- Monitoring: Uptime Kuma + Global Grafana

[![Monitoring: Uptime Kuma + Global Grafana](https://img.youtube.com/vi/cBWgi_J1zM8/0.jpg)](https://www.youtube.com/embed/cBWgi_J1zM8?si=U8OCnHJ-6hS1b_Uk)

- Backup: Duplicati + Telegraf + InfluxDB + Grafana

[![Backup: Duplicati + Telegraf + InfluxDB + Grafana](https://img.youtube.com/vi/rWEDQd0qn2c/0.jpg)](https://www.youtube.com/embed/rWEDQd0qn2c?si=U8OCnHJ-6hS1b_Uk)

- MQTT: Mosquitto + EMQX

[![MQTT: Mosquitto + EMQX](https://img.youtube.com/vi/mgSjszDx8S8/0.jpg)](https://www.youtube.com/embed/mgSjszDx8S8?si=U8OCnHJ-6hS1b_Uk)

- Automation: Node-RED (Git based flows)

[![Automation: Node-RED (Git based flows)](https://img.youtube.com/vi/P1uduhdSG1o/0.jpg)](https://www.youtube.com/embed/P1uduhdSG1o?si=U8OCnHJ-6hS1b_Uk)

- Development base image: Ansible creation base image

[![Development base image: Ansible creation base image](https://img.youtube.com/vi/bW0RQB9-xr4/0.jpg)](https://www.youtube.com/embed/bW0RQB9-xr4?si=U8OCnHJ-6hS1b_Uk)

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
- Integrate all services behind NGINX and manage it with NGINX UI: https://github.com/0xJacky/nginx-ui
- New theme for OpenWRT: Argon - https://github.com/jerrykuku/luci-theme-argon

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
