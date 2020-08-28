# Welcome to my Homelab!

Hello stranger! You've arrived at my repository where I document my on-going projects within my homelab. I hope you find my work interesting and leave with learning something. Let's get right into it!

## Infrastructure

I'm going to split this part into two sections, physical and virtual. This will give you a clear picture on the high-level components and its underlying hardware.

### Physical

- Dell R710 loaded with Proxmox
  * 2 x Intel Xeon E5530
  * 12 x 16gb RAM
  * 6 x 500gb SAS HD
  * 2 x 250gb SATA HD
- PCEngine apu4d4 loaded with pfSense
- TP-Link Managed Switch
- Unifi AP AC LR
- 2 x TrippLite APCs
- Synology 2-Bay 16 TB/ 20 TB Network Attached Storage (DS216play)
- Raspberry Pi 3 (ns1) - Primary BIND DNS server

### Virtual

- heracles: OpenLDAP Server
- ns2: Secondary BIND Server
- artemis: Utility Server
  * Nessus
  * OpenVAS
  * unifi
- minio-arch: Minio Storage Server
- plutus: Debian Misc Server
- hermes: HAProxy Load Balancer
- jellyfin: Jellyfin Media Server
- cerebus: OpenVPN Client to IVPN
- athena: CI/CD Server
  * Ansible
  * Terraform
  * Gitlab CI agent
- kubemaster01: Kubernetes master node
- kubeworker01: Kubernetes worker node
- kubeworker02: Kubernetes worker node
- kubeworker03: Kubernetes worker node
