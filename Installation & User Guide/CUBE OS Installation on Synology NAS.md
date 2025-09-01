## Prerequisites
+ **Hardware**:
    - At least **6GB RAM** installed in your Synology NAS (_4GB allocated for the virtual machine_). If your NAS has only 2GB or less, consult Synology's upgrading guides.
    - Your Synology NAS must have an **x64 platform** (modern units with Intel or AMD processors). 
+ **Software**:
    - WAN access to download the Virtual Machine Manager from the Synology Package Center.
    - Admin account access to your Synology NAS.
    - **CUBE OS Image**: Download the latest `.xz` image file from the Git repository, then extract it to obtain the `.vdi` disk image for use.

## Installing Virtual Machine Manager
1. Access the Synology NAS **dashboard** via a web browser.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1749436332162-4ec06a98-76d1-4323-be6a-123d9cd92eba.png)

2. Install the **Virtual Machine Manager** package from the Synology Package Center.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1749436396792-55b19910-b038-4888-8238-04455dd7bf9d.png)

3. Launch **Virtual Machine Manager** from the NAS dashboard.

## Creating the Virtual Machine
1. Navigate to the **Image** page.
2. Switch to the **Disk Image** tab and click the **Add** button.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1749436628664-e614b162-1529-4803-900a-df1dea5ce8c0.png)

3. Follow the prompts to upload the CUBE OS `.vdi` file.

_Note: you have to unzip the .xz file first!_

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1749436689559-5f3f77b6-b47b-4240-b7e1-4f4c8a6bd24b.png)

4. Once the image upload is complete, switch to the **Virtual Machine** page.
5. Click the dropdown icon next to the **Create** button and select **Import**.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1749436814949-6f1b9f91-c28e-4fbe-b9fe-320618c6eeb9.png)

6. In the wizard, choose **Import from Disk Images**.
7. Select the storage location where you uploaded the virtual disk file.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1749436853839-550f06de-994d-47c1-8d29-5272510c43d7.png)

## Configure Virtual Machine Settings
1. Assign computational resources to CUBE OS: 
    - **vCPUs**: 2 cores
    - **RAM**: 4GB

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1749436943605-ae5db23c-2a07-4e28-9cd3-c2a672e951d7.png)

2. Choose the **Default VM Network**.
3. In the **Firmware** option, select **UEFI** to ensure compatibility.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1749437240803-2cf20b1d-b5cc-4283-b34b-a0613c49164b.png)

4. To connect your Zigbee devices, plug the dongle into your NAS via USB and pass it through to the virtual machine on this page.
5. Assign management permissions to your NAS accounts.
6. Review all settings and ensure the **Power on the virtual machine after creation** option is selected.
7. Click **Done** to complete the setup.

## Booting CUBE OS
1. Wait for a few minutes while the virtual machine powers on.
2. Open a web browser and enter `http://cube.local` to access the CUBE OS onboarding page. 
    - Alternatively, you can use the CUBE OS's IP address to access the page.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1748425757582-90bb0b5e-2065-4518-a222-1315dee167ba.png?x-oss-process=image%2Fformat%2Cwebp)

3. Upon successful access, navigate to the **Settings** page. Here, you will find a **short ID** for your instance.
4. To manage multiple CUBE OS instances on the same network, use the URL `http://cube-{shortID}.local`.

