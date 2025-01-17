# Cisco Packet Tracer on Void Linux

Following https://github.com/void-linux/void-packages/issues/39294, I tried to improve an already existing Cisco Packet Tracer unofficial installer for Void Linux.

**Tested with Cisco Packet Tracer 820 for Ubuntu 64 bit on Void Linux x86_64**

![Shellcheck workflow](https://github.com/clyhtsuriva/void-packettracer/actions/workflows/shellcheck-actions.yml/badge.svg)

## Prerequisites

- CiscoPacketTracer_*.deb - Available on [NetAcad](https://www.netacad.com/portal/resources/packet-tracer) (**account needed**)
- xz - XZ compression utilities
- xdg-utils - Tools to assist applications with various desktop integration tasks
- binutils - GNU binary utilities - containing ar

### Depedencies installation command

```sh
xbps-install -S xz xdg-utils binutils
```

## Installation

```sh
curl -LO https://raw.githubusercontent.com/clyhtsuriva/void-packettracer/master/install_pt.sh
chmod +x ./install_pt.sh
./install_pt.sh <.deb file>
```

## Running

```sh
/opt/pt/packettracer
```

## Uninstallation

```sh
curl -s https://raw.githubusercontent.com/clyhtsuriva/void-packettracer/master/uninstall.sh | sudo bash
```
