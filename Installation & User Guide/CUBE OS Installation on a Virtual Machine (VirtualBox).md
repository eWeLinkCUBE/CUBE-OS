## Prerequisites
+ **Hardware**:
    - Minimum 4 GB RAM and a dual-core CPU.
    - At least 32 GB free disk space.
+ **Software**: 
    - Oracle VirtualBox (recommended) or any other hypervisor you are comfortable with.
    - **CUBE OS Image**: Download the latest CUBE OS `.zip` or `.xz` archive from: Git repository: `[Link]`

## Installing VirtualBox
1. Download the VirtualBox installer from the [official website](https://www.virtualbox.org/).
2. Run the installer and follow the on-screen prompts.
3. After installation, launch VirtualBox and verify the version (`Help → About VirtualBox`).

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748427226070-9e5c7fa2-0b9a-45bb-9ebe-54adffc7e52c.png)

## Creating the Virtual Machine
1. Open VirtualBox and click **Machine → New** (or press **Ctrl + N**).

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748427301419-3553955a-6a9b-493e-a1be-2bb9cf32064a.png)

2. **Name and OS Type:**
    - **Name:** CUBE OS
    - **Type:** Linux
    - **Version:** Other Linux (64-bit)

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748427420975-e482a1a8-95ce-43e2-bed0-cb319882c3d8.png)

3. **Memory:** Allocate **4 GB** of RAM (4096 MB).
4. **Processors:** Assign **2** CPU cores (Settings → System → Processor).
5. **Enable EFI:** Under **System → Motherboard**, check **Enable EFI**.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748427527771-5c45fde7-dc20-4298-b19d-2630def8e8d3.png)

**Important:** CUBE OS requires EFI to boot correctly

6. **Hard Disk:** Choose **Use an existing virtual hard disk file**, then browse to the extracted `.vdi` image.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748428014437-15772c94-4a44-451c-b29a-9eeeef36cf5b.png)

7. Click **Create** to finish the VM setup.

## Configuring the Virtual Machine
1. Select the newly created VM and click **Settings**.
2. **Network:** Under **Network**, set **Attached to** → **Bridged Adapter** and select your active physical NIC.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748428072657-ea96e707-4d18-4d12-acc9-b3229272fd45.png)

3. **Audio:** Under **Audio**, enable audio and choose **Intel HD Audio** as the controller.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748428110254-7d11a0d3-4db3-4a69-9c72-c4d7df8a7d8b.png)

4. **USB (Optional):**
    - To use a Zigbee dongle, insert it into a USB port.
    - In **USB**, enable the appropriate USB controller (USB 2.0 or 3.0).
    - Click the **+** icon in **USB Device Filters** and select your Zigbee dongle from the list.
5. Click **OK** to save all settings.

## Booting CUBE OS
1. In VirtualBox, select your CUBE OS VM and click **Start**.
2. Watch the console; the system will initialize and mount partitions.
3. When the boot sequence completes, you will hear a short chime and see the CUBE OS IP address displayed on screen.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748428170502-de3d01a9-f83d-4510-a298-e7790bb7a06b.png)

## Accessing the CUBE OS Web Interface
1. Open a browser on any host in the same network.
2. Enter the displayed IP address (e.g., `http://192.168.1.42`) or use mDNS: `http://cube.local`.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748425757582-90bb0b5e-2065-4518-a222-1315dee167ba.png)

3. On first access, navigate to **Settings → System Info** to view your device's short ID.
4. You can also reach your instance via `http://cube-<shortID>.local` (useful when multiple CUBEs are on your LAN).

## Troubleshooting
| Issue | Possible Cause | Solution |
| --- | --- | --- |
| VM fails to start | EFI disabled | Enable EFI in **Settings → System** |
| No network connectivity | Wrong adapter mode | Select **Bridged Adapter** & correct NIC |
| No IP displayed after boot | DHCP issues or service failure | Check router DHCP; reboot VM |
| Zigbee dongle not detected | Missing USB filter | Add filter under **USB** settings |
| CUBE OS web UI not reachable | Firewall or wrong URL | Use `cube.local`<br/> or IP; disable host firewall |




