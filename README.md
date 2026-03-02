# Homelab Infrastructure

A production-grade virtualized infrastructure built on Proxmox VE, including virtualization, network security, self-hosted services, and zero-trust networking principles.

## 🎯 Project Overview

This homelab serves as a practical learning environment for modern infrastructure technologies.

## 🚀 Services Deployed

### Network Services
- **Pi-hole**: Network-wide DNS filtering and ad-blocking
  - Custom DNS records for internal services
  - DHCP server for network management
  - Query logging and analytics dashboard

- **Windows AD Server**: Centralized management platform for 

### Security & Remote Access
- **WireGuard VPN**: Secure remote access to homelab resources
  - Point-to-point encrypted tunnels
  - Multi factor authentication system
  - Firewall rules for secure access
  - Fail2ban to prevent flooding or DoS attacks.

- **Security and Cryptography**
  - Self signed SSL certs
  - Asymmetric key based SSH encryption and authentication

- **Tailscale**: Zero-config mesh VPN
  - Cross-platform device connectivity
  - ACL-based access control
  - Integration with existing network services
  - MagicDNS

- **Vaultwarden**: Self hosted passwords manager
  - Cross platform solution for password/secrets.
  - Custom KDF setup.
  - Encrypted vaults.
  - Smaller resource footprint.


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
- Virtualization and containerization technologies
- Network design and security implementation
- VPN configuration and zero-trust networking
- Service deployment and configuration management
- Backup and disaster recovery planning
- Infrastructure documentation and maintenance

## 🔄 Future Improvements

- [ ] Implement Prometheus + Grafana monitoring stack
- [ ] Add centralized logging with ELK/Loki
- [ ] Automate VM provisioning with Terraform
- [ ] Implement CI/CD pipeline for service updates
- [ ] Add redundant storage with Ceph or GlusterFS
- [ ] Create automated disaster recovery procedures
- [ ] Implement Infrastructure-as-Code with Ansible

## 📚 Documentation

Detailed documentation for each component can be found in the `/docs` directory:

- [Architecture Overview](docs/architecture.md)
- [Network Configuration](docs/networking.md)


## 🤝 Contributing

This is a personal learning project, but suggestions and feedback are welcome! Feel free to open an issue if you have questions or recommendations.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

**Note**: This homelab is used for educational purposes and continuous learning in IT infrastructure and DevOps practices. All configurations are sanitized to remove sensitive information.
