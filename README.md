# Reverse Proxy

This role sets up a reverse proxy, to route HTTP traffic to the containers.
Currently this is facilitated by traefik.

## Requirements

A working Docker installation on the host system is all you need.
For automatic certificate generation via LetsEncrypt a domain name has to point toward your host address.

## Configuration Variables

```yaml
path: "/home/user/reverseproxy" # Where the VPN proxy service will reside
data: "/data/reverseproxy/cert" # Where the certificates will be persisted
conf: "/data/reverseproxy/conf" # Where the configuration will be persisted
letsencrypt_email: "root@example.com" # Email of the admin, will be used for notifications
```

## Upgrading installations

To upgrade the installation it is sufficient to simply run this playbook again after increasing
the version number.
