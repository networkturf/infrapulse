---
layout: post
title: "Getting Started with Ansible for Network Automation"
date: 2024-01-15
author: Kunal Vaidya
tags:
  - Ansible
  - Automation
  - Networking
  - DevOps
---

Ansible has become one of the most popular tools for network automation. In this post, we'll explore the basics of getting started with Ansible for managing network devices.

## Why Ansible?

Ansible is an agentless automation tool that uses SSH to connect to devices. This makes it perfect for network automation since most network devices support SSH out of the box.

## Installation

First, let's install Ansible:

```bash
pip install ansible
```

For network automation, you'll also want to install the network collection:

```bash
ansible-galaxy collection install cisco.iosxr
```

## Basic Playbook Structure

Here's a simple playbook to get you started:

```yaml
---
- name: Configure BGP on Router
  hosts: routers
  gather_facts: false
  tasks:
    - name: Configure BGP neighbor
      cisco.iosxr.iosxr_config:
        lines:
          - router bgp 65000
          - neighbor 192.168.1.1 remote-as 65001
          - address-family ipv4 unicast
        commit: yes
```

## Best Practices

1. **Use inventory files** to organize your devices
2. **Leverage roles** for reusable configurations
3. **Use variables** to make playbooks flexible
4. **Test in a lab environment** before production

## Next Steps

Once you're comfortable with the basics, explore:
- Ansible roles for complex configurations
- Jinja2 templates for dynamic configurations
- Ansible Vault for secure credential management

Happy automating!

