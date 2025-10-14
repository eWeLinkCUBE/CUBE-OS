# eWeLink CUBE OS

**eWeLink CUBE OS** is a Smart Home Platform for local small-scale computing platforms, tailored and optimized from the eWeLink Smart Home Cloud Platform and hardware-adapted.

Originally built into SONOFF iHost, CUBE OS is now available as a standalone system you can install on platforms like Raspberry Pi, virtual machines, and NAS devices.
<img width="2620" height="1500" alt="eWeLink CUBE OS" src="https://github.com/user-attachments/assets/104b3dab-277e-4dfe-8c0b-125ed46f937c" />


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

Refer to the [Installation Guide](https://github.com/eWeLinkCUBE/CUBE-OS/tree/master/Installation%20%26%20User%20Guide) for detailed platform-specific steps.

## 🧰 Getting Started

1. **Download the image** for your device from the [Releases](https://github.com/eWeLinkCUBE/CUBE-OS/releases) page
2. **Flash or mount** the image using tools like Raspberry Pi Imager, Etcher, or your hypervisor’s disk manager
3. **Boot the device** and wait for the system to initialize
4. **Access the Web UI** via `http://cubeos.local` or your device’s IP address

## 🧪 Beta Participation

We're currently running a **public beta** for CUBE OS v0.4. Testers can:

- Help shape the future of local-first smart home automation

<img width="2160" height="1600" alt="EDM：Join CUBE OS Beta Test,Win a Zigbee Dongle@2x" src="https://github.com/user-attachments/assets/4c7c2355-95cb-46ff-b519-d77f804f736f" />

To participate:
- Download, install, and start testing!
- [Join our Discord](https://discord.gg/67Ybdn23rS)
- [Fill out this survey](https://docs.google.com/forms/d/e/1FAIpQLSdSTEeWK2Pmyz01FMwFzZkh7zwor0tHGhaAzSurkqmdTamNLQ/viewform?usp=sharing&ouid=100134271027504904332)

## 🧱 Architecture

CUBE OS is designed with performance and modularity in mind:

- **Core System**: Lightweight OS built with Buildroot
- **Apps**: Independent system modules running as isolated processes
- **Messaging Layer**: Internal middleware to enable high-efficiency communication between apps
- **Zigbee2CUBE**: Middleware to support multiple Zigbee protocols and chipsets via modular drivers
- **Docker Runtime**: For containerized third-party applications and add-ons
- **Web API Layer**: Built-in OpenAPI interface for inter-module and external integration
- **Deployment Flexibility**: Runs in smart home hubs or edge computing scenarios with local or centralized device control

## 🛠️ Common Use Cases

- Pair Zigbee devices via supported USB dongles (e.g., SONOFF ZBDongle-E)
- Use CAST dashboards to control devices from tablets, kiosks, or wall-mounted screens
- Create local scenes and automations
- Extend system with Docker-based add-ons
- Access data via Web API for integration with other platforms

## 🧯 Troubleshooting & Support

- Can't access the Web UI? Try using the device’s IP address instead of `cubeos.local`
- Zigbee issues? Check dongle connection and firmware compatibility
- Need help? Ask questions or report issues in our [Discord](https://discord.gg/67Ybdn23rS)

## 🙌 Contribute

We welcome feedback and contributions! If you'd like to help improve CUBE OS, feel free to open issues, suggest enhancements, or fork the repo.

> Built with ❤️ by the eWeLink team
