## Prerequisites
+ **Hardware:**
    - Raspberry Pi 4B or 5 (Pi 3 and below not recommended)
    - Official 5 V/3 A USB‑C power supply
    - Recommended Class A2 microSD card (≥32 GB)
    - microSD card reader
    - Ethernet cable
+ **Software:**
    - Download the latest CUBEOS `.xz` archive.
    - Raspberry Pi Imager (or alternative flashing tool)

**Note:** Avoid using generic phone chargers or USB ports on PCs—they often cannot deliver the sustained current required by the Pi.

## Prepare the Micro SD Card
1. Insert your microSD card into the USB card reader and connect it to your computer.
2. Download Raspberry Pi Imager from [raspberrypi.org](https://www.raspberrypi.com/software/).
3. Launch Imager and ensure you have the latest version (v1.8+).

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748424022489-1cd1f4c9-d9c8-42b9-8fcb-8c3ea8e4122c.png)

## Flash CUBEOS Image
1. In Raspberry Pi Imager, <font style="color:rgb(31,35,40);">click </font>**<font style="color:rgb(31,35,40);">CHOOSE DEVICE > No filtering</font>**<font style="color:rgb(31,35,40);">. </font>Click **CHOOSE OS → Use custom**, then select the downloaded CUBEOS Beta image (`.img` or compressed archive).

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748424055477-6537f1c5-da6d-46f7-a7fa-052185507fc6.png)

2. Click **CHOOSE STORAGE** and select your microSD card (double‑check to avoid overwriting other drives). Click **NEXT** > **NO**, **CLEAR SETTINGS**, and confirm to erase all settings on the SD card<font style="color:rgb(31, 35, 40);">.</font>

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748424080114-73d9c060-30ec-45a5-979b-a0b81810999f.png)

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748424975730-a7500f96-19e2-4a3d-8db3-a9411256b93f.png)

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748425025519-0dd6d967-823d-4e48-b25e-3aba1f90450b.png)

3. Click **Write**, confirm, and wait for the process to complete.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748425049287-61fecfef-2bdc-463d-830a-a19b4eaf018d.png)

**Tip:** Do not remove the card or interrupt the write. Typical flashing time: 3–5 minutes.

## Booting CUBEOS
1. Insert the flashed microSD card into the Pi and connect the Ethernet cable (or configure Wi‑Fi via Imager).

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748425383341-0121488d-4ac0-465b-a93a-083606070b93.png)

2. Power on the Pi using the official 5 V/3 A adapter.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748425441273-22b76a34-5487-4d66-9952-059d6f2b4a7e.png)

3. Observe the LEDs:
    - **Red steady:** Power OK
    - **Green blinking:** SD card activity (normal boot)
4. Wait up to 2 minutes for the system to initialize.

## Access the Web Interface
1. On a computer in the same network, open a browser.
2. Navigate to `http://cube.local` or the IP shown via your router (e.g., `http://192.168.1.42`).

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748425757582-90bb0b5e-2065-4518-a222-1315dee167ba.png)

3. On first access, navigate to **Settings → Gateway Info** to view your device's short ID.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750062038325-53086122-c940-4d3f-ab8d-bb9ba7f43154.png)

4. You can also reach your instance via `http://cube-<shortID>.local` (useful when multiple CUBEs are on your LAN).

## Troubleshooting
| Issue | Cause | Solution |
| --- | --- | --- |
| No power (no red LED) | Faulty power supply or cable | Use official 5 V/3 A USB‑C adapter & cable |
| Green LED off | SD card not detected or image not flashed | Reflash card; ensure firm card seating |
| Green LED solid (no blink) | Corrupted image | Redownload and reflash CUBEOS image |
| Cannot reach `cube.local` | mDNS conflict or disabled service | Use IP address; check DNS/mDNS settings |
| Web UI inaccessible after 5 min | Boot hang or network issue | Check Ethernet cable; ping Pi’s IP; reboot Pi |


