# eWeLink CUBE OS

**eWeLink CUBE OS** is a Smart Home Platform for local small-scale computing platforms, tailored and optimized from the eWeLink Smart Home Cloud Platform and hardware-adapted.

Originally built into SONOFF iHost, CUBE OS is now available as a standalone system you can install on platforms like Raspberry Pi, virtual machines, and NAS devices.

## 🚀 Key Features

- **Zigbee support** with USB dongles (e.g. SONOFF ZBDongle-E)
- **Matter Hub & Matter Bridge** for local Matter control
- **CAST dashboards** for intuitive device control
- **Remote access/Push Notification** via PWA (no cloud dependency)
- **Scene automation, device grouping, and backups**
- **Add-on ecosystem** powered by Docker

## 💻 Supported Platforms

CUBE OS can be installed on:

- **Raspberry Pi 4B / 5** (Recommended: 4 GB RAM or higher)
- **Virtual Machines** (x86_64 architecture, e.g. VirtualBox / VMware)
- **NAS devices** (with compatible CPU and UEFI boot support)

## 🧰 Getting Started(Raspberry Pi as an example)

1. **Download the image**
   - Visit the [Releases](https://github.com/eWeLinkCUBE/CUBE-OS/releases) page to get the latest image for your platform

2. **Flash to device**
   - Use tools like [Raspberry Pi Imager](https://www.raspberrypi.com/software/) or [Balena Etcher](https://etcher.io/) to flash the image to your SD card or virtual disk

3. **Boot and access CUBE OS**
   - Once installed, boot the device and access the dashboard from your browser.

4. **Join the community**
   - [Join Discord](https://discord.gg/67Ybdn23rS) to share feedback, report issues, or get help

## 🧪 Beta Participation

We're currently running a **public beta** for CUBE OS v0.4. Testers can:

- Help shape the future of local-first smart home automation

<img width="2160" height="1600" alt="EDM：Join CUBE OS Beta Test,Win a Zigbee Dongle@2x" src="https://github.com/user-attachments/assets/4c7c2355-95cb-46ff-b519-d77f804f736f" />

To participate:
- Download, install, and start testing!
- [Join our Discord](https://discord.gg/67Ybdn23rS)
- [Fill out this survey](https://docs.google.com/forms/d/e/1FAIpQLSdSTEeWK2Pmyz01FMwFzZkh7zwor0tHGhaAzSurkqmdTamNLQ/viewform?usp=sharing&ouid=100134271027504904332)

## 🧱 Architecture

CUBE OS is built with modularity and security in mind:

- **Base OS**: Buildroot-based minimal Linux system
- **Containerized core**: All services run in Docker (including the CUBE Engine, CAST, and Zigbee services)
- **Add-on Framework**: Add-ons and integrations can run in isolated containers
- **Zigbee/Matter abstraction**: Supports popular USB dongles and bridges

## 🛠️ Common Tasks

- Access file system via Samba or SSH
- Install add-ons like File Browser or MQTT broker
- Use CUBE CAST to build custom dashboards
- Set up Zigbee pairing via supported dongles
- Configure Matter Bridge via UI wizard

## 🧯 Troubleshooting

- Zigbee not pairing? Make sure your dongle firmware is up to date
- Network issues? Check that the CUBE container has internet and LAN access

Report bugs or ask questions in our [Discord](https://discord.gg/67Ybdn23rS)

## 🙌 Contribute

We welcome feedback and contributions! If you'd like to help improve CUBE OS, feel free to open issues, suggest enhancements, or fork the repo.

> Built with ❤️ by the eWeLink team
