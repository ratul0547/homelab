# Homelab Infrastructure

A production-grade virtualized infrastructure built on Proxmox VE, including virtualization, network security, self-hosted services, and zero-trust networking principles.

## 🎯 Project Overview

This homelab serves as a practical learning environment for modern infrastructure technologies.

## 🚀 Services Deployed

### Network Services
- **Pi-hole**: Network-wide DNS filtering and ad-blocking
  - Custom DNS records for internal services
  - Query logging and analytics dashboard
- **Caddy**: Automatic reverse proxy
  - Automatic secure HTTPS reverse proxy to servers
  - Self signed certificates management
- **NFS Server**: Network File Sharing
  - Secure file Sharing server over the network
  - NFS server deployed using Open Media Vault from ZFS pool
- **Tailscale**: Zero trust mesh VPN
  - A dedicated server as exit node to securely connnect to the internet
  - Used NAT and separate subnet to isolate exit node traffic
  - LAN subnet advertising enabled to make devices available without installing tailscale
  - ACL rules to harden security and access
  - MagicDNS settings to make management of devices and services easier
  

### Security & Remote Access
- **WireGuard VPN**: Secure remote access to homelab resources
  - Point-to-point encrypted tunnels
  - Multi factor authentication system

- **Security and Cryptography**
  - Self signed SSL certs to make connections secure and encrypted.
  - Asymmetric key based SSH encryption and authentication.
  - Fail2ban to prevent flooding or DoS attacks.
  - Firewall whitelist rules for secure access. Deny by default policy.
 
- **Active Directory Server**: Windows active directory server for centralized identity management
  - MS Windows Server 2025 as the OS. (Recently upgraded from Windows Server 2022).
  - Centralized user and group policy management for home users and other Windows servers.
  - Secure and automated management of all machines in the OU with powershell scripts.

- **Vaultwarden**: Self hosted Bitwarden compatible passwords manager server (Formerly bitwarden_rs)
  - Cross platform solution for password/secrets.
  - Custom KDF setup.
  - Encrypted database known as vaults.
  - Smaller resource footprint.
  - MFA Authentication, FIDO2, YubiKey Support.


### Self-Hosted Applications
- **Nextcloud**: Private cloud storage and collaboration platform
  - File synchronization across devices
  - Calendar and contacts management
  - Secure file sharing with external users
 
- **Immich**: Private Images and videos backup solution
  - Automatic images and videos backup accross devices
  - Manage Duplicates
  - Multi user support

### Virtualization Platform
- **Proxmox VE**: Enterprise virtualization environment
  - Multiple VMs and LXC containers
  - Resource management and allocation
  - Backup and snapshot capabilities

## 💻 Technology Stack

| Category | Technologies |
|----------|-------------|
| **Virtualization** | Proxmox VE, KVM, LXC Containers |
| **Operating Systems** | Ubuntu Server, Debian, Alpine Linux, Fedora Server, Windows Server |
| **Networking** | WireGuard, Tailscale, Pi-hole, VLANs, NAT, Reverse proxy |
| **Storage** | ZFS, LVM, NFS |
| **Security** | UFW, fail2ban, SSL/TLS certificates |
| **Services** | Nextcloud, Vaultwarden, Immich, Docker, Podman, Nginx, Apache, Active Directory |

## 📋 Key Features & Capabilities

- **High Availability**: Service isolation in separate VMs/containers for fault tolerance
- **Security**: Multi-layered security with VPN, DNS filtering, and firewall rules
- **Automation**: Scripted deployments and automated backups
- **Monitoring**: Service health checks and resource utilization tracking
- **Scalability**: Modular design allowing easy addition of new services

## 🎓 Skills Demonstrated

- Linux system administration and troubleshooting
- Windows server administration and troubleshooting
- Identity management with Active Directory
- Virtualization and containerization technologies
- Network design and security implementation
- VPN configuration and zero-trust networking
- Service deployment and configuration management
- Backup and disaster recovery planning
- Infrastructure documentation and maintenance

## 🔄 Future Improvements

- [ ] Implement Grafana monitoring stack
- [ ] Add centralized logging with Loki
- [ ] Automate VM provisioning with Terraform
- [ ] Add redundant storage with Ceph
- [ ] Create automated disaster recovery procedures

## 📚 Documentation

Detailed documentation for each component can be found in the `/docs` directory:

- [Architecture Overview](docs/architecture.md)
- [Network Configuration](docs/networking.md)


## 🤝 Contributing

This is a personal learning project, but suggestions and feedback are welcome! Feel free to open an issue if you have questions or recommendations.


---

**Note**: This homelab is used for educational purposes and continuous learning in IT infrastructure and DevOps practices. All configurations are sanitized to remove sensitive information.
