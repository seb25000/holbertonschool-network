# Networking Basics #1

## Description

This project explores fundamental networking concepts by implementing basic network tasks using Bash scripts. The tasks involve modifying IP configurations, displaying network information, and listening on specific ports. The project provides hands-on experience with concepts such as `localhost`, IP addresses, and basic network services on an Ubuntu machine.

### Learning Objectives

By the end of this project, you will be able to explain:

- **What is localhost/127.0.0.1**: The default IP address used to refer to the current system.
- **What is 0.0.0.0**: An address that represents all available IPv4 addresses on a networked machine.
- **What is /etc/hosts**: A file used by the operating system to map hostnames to IP addresses.
- **How to display your machine’s active network interfaces**: Using `ifconfig` or other networking tools.

## Requirements

- The project files are compatible with **Ubuntu 20.04 LTS**.
- All Bash scripts must be executable and pass Shellcheck (`version 0.7.0` via `apt-get`) without errors.
- The first line of all Bash scripts is `#!/usr/bin/env bash`.
- Each script contains a comment explaining its purpose.

## Tasks

### 0. Change your home IP

Write a Bash script that configures the following:

- `localhost` resolves to `127.0.0.2`.
- `facebook.com` resolves to `8.8.8.8`.

#### Example:
```bash
ping localhost
# Outputs: PING localhost (127.0.0.2)
ping facebook.com
# Outputs: PING facebook.com (8.8.8.8)
```

**File**: `0-change_your_home_IP`

### 1. Show attached IPs

Create a Bash script that displays all active IPv4 IP addresses on the machine it is executed on.

#### Example:
```bash
./1-show_attached_IPs
# Outputs: 127.0.0.1, 10.0.2.15 (or other IPs depending on the system configuration)
```

**File**: `1-show_attached_IPs`

### 2. Port listening on localhost

Write a Bash script that listens on port 98 on `localhost`. This task demonstrates how to create a simple TCP server that can accept connections and display messages sent via a client.

#### Example:
- **Terminal 0**: Start the script listening on port 98.
```bash
sudo ./2-port_listening_on_localhost
# Output: Listening on port 98...
```
- **Terminal 1**: Connect to `localhost` on port 98 using `telnet` and send some messages.
```bash
telnet localhost 98
# Outputs: Connected to localhost.
```

**File**: `2-port_listening_on_localhost`

## How to use

1. Clone the repository:
   ```bash
   git clone https://github.com/nihadamirov/holbertonschool-network
   ```

2. Navigate to the project directory:
   ```bash
   cd basics_1
   ```

3. Make the scripts executable:
   ```bash
   chmod +x *.sh
   ```

4. Run each script to perform the specific task.

## Resources

- [What is localhost](https://en.wikipedia.org/wiki/Localhost)
- [What is 0.0.0.0](https://en.wikipedia.org/wiki/0.0.0.0)
- [Netcat examples](https://www.geekstuff.net/2012/04/nc-command-examples)
- Ubuntu `man` pages: `ifconfig`, `telnet`, `nc`, `cut`.


