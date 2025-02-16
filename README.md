# NOTICE

This is script is under developement so issues and problems are common - if you had any problems kindly issue it

# Easy Node

This script sets up nodes for the Marzneshin and Marzban panels.

## Features

- Supports a variety of CPU architectures
- Allows for custom core versions for Sing-box Hysteria Xray
- Provides a control script for managing nodes (start, stop, restart)
- Uses a single directory for easier management

Generate cert and key for hysteria :
```bash
cd /var/lib/masoud/hysteria

openssl req -x509 -newkey rsa:4096 -keyout key.pem -out cert.pem -sha256 -days 3650 -nodes -subj "/C=XX/ST=StateName/L=CityName/O=CompanyName/OU=CompanySectionName/CN=CommonNameOrHostname"

```


## Installation

**Run the script as root:**

For Marzneshin:
```bash
bash <(curl -Ls https://raw.githubusercontent.com/Masouuuuuuud/my-ez-node/refs/heads/slave/marznode.sh)
```

For Marzban:
```bash
bash <(curl -Ls https://raw.githubusercontent.com/mikeesierrah/ez-node/main/marzban-node.sh)
```

## Directory Structure

**Marznode:**
```
/var/lib
        └── your-node-name
                ├── .env
                ├── docker-compose.yml
                ├── client.pem
                |
                ├── sing-box
                │    └── sing-box core
                ├── xray
                │    ├── xray core
                │    └── xray assets
                └── hysteria
                    └── hysteria core
```

**Marzban-node:**
```
/opt/marzban-node
        └── your-node-name
                ├── .env
                ├── docker-compose.yml
                ├── client.pem
                |
                └── xray core
```

## Control Script

This script also installs a control script in your system's PATH.

### Usage:

For Marznode:
```bash
marznode <node-name> restart | start | stop
```

For Marzban-node:
```bash
marzban-node <node-name> restart | start | stop
```
## Donation

If you'd like to show your appreciation, please donate $5 to someone in need.
