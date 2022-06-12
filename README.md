# ansible-ubuntu-loopback
Ansible role to add IP addresses on loopback interface in Ubuntu

## Installation

Create requirements.yml file

```
# Include ubuntu-loopback role
- src: https://github.com/FastMT/ansible-ubuntu-loopback.git
  name: ubuntu-loopback
  version: "v1.0.0"
```

Install external module into ~/.ansible/roles folder

```
ansible-galaxy install -r requirements.yml
```

## Usage

playbook.yml:

```
# Configure IP addresses on loopback interface
- role: "ubuntu-loopback"
    vars:    
      # IP addresses to be configured on loopback interface
      # 127.0.0.1/8 is already set by default
      loopback_ip_addresses:
        - "10.0.0.1/24"
```        