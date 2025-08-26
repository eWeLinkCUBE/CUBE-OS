## Prerequisites
+ **Hardware:**
    - Ugreen NAS with **x86 architecture**, such as DXP2800
    - **At least 6GB of RAM** (4GB or more should be allocated to the virtual machine)
    - USB port available if using Zigbee/Thread dongle
+ **Software:**
    - Virtual Machine feature must be supported and enabled
    - Admin access to your NAS
    - Download the latest `.xz` image file from the Git repository, then extract it to obtain the `.vdi` disk image for use.

---

## 2. Installing Virtual Machine Feature
1. Log into your Ugreen NAS web dashboard.
2. Navigate to the **Virtual Machine Manager** and open it.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384129105-2cb12283-9ca2-45d7-855b-d8f88e079207.png)

---

## 3. Creating the Virtual Machine
1. Click **Create VM**, then select **Import Virtual Machine**.
2. Choose **Import from Disk File**, then click **Next**.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384323271-263e6dfe-6d88-4468-8c5c-a5e7b499035a.png)

3. If this is your first time setting up, select **Upload image manually**.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384372767-cdc4871f-4ca6-4046-a49b-7ad612ff0bb9.png)

4. Locate the downloaded CUBE OS `.vdi` file:
+ You can upload it from your local device, or
+ Select it from existing files on your NAS.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384414341-fb1e2a4e-4280-4644-a48c-ffcb12695623.png)

5. After selecting the image, click **Confirm** to upload and convert the image.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384445651-a092923b-18db-414e-9803-ba7e68486115.png)

6. Once imported, repeat the **Import Virtual Machine** process:
+ The uploaded image will now appear in the dropdown list.
+ Select it and click **Next**.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384596652-d24d1c87-28f7-402b-aa5c-e6b62ae68fbb.png)

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384627062-bb6fee9e-7c5a-4d57-b083-fc0ff4c5e321.png)

7. Choose a storage volume for the virtual machine and continue.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384735371-df124e37-3049-4f9a-bcda-fa911e40c354.png)

---

## 4. Configure Virtual Machine Settings
1. Basic Configuration:
+ **System type**: Select **Other**
+ **vCPUs**: 2 cores (or more if available)
+ **Memory**: Allocate **4GB or more**

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384764354-befd9258-07ef-45d1-8d5d-acc15942753c.png)

2. Network Configuration:
+ Select **Bridge mode** (Do **not** use Host or NAT)

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384784190-ae4fc0e7-c485-42d8-990d-0039135e947f.png)

3. Under USB options, locate and add your Zigbee/Thread USB dongle:
+ Click the **+** icon to assign the correct USB port.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384809712-771aeb4d-cdad-43d3-a0e8-90477cc74d81.png)

4. Set **Bootstrap Type** to **UEFI**.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384824921-cb1d8dfc-f065-489d-ae5d-0e3128bddcf2.png)

5. Click **Done** to finish setup.

---

## 5. Booting CUBE OS
1. Back in the VM list, click **Start** to power on the virtual machine.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384913122-696274fe-1600-4748-afc9-7d4faa9a5a6e.png)

2. Monitor the CPU and RAM usage if needed.
3. Click **Connect** to view the VM console:
+ If the CUBE OS welcome screen appears, the system has started successfully.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384947150-fe737f39-85b9-4456-a5a6-6afba145049d.png)

4. On another browser tab:

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1754384967592-4bf694b4-0c9b-44df-b785-bc1589e123c1.png)

+ Enter the **VM’s IP address** (e.g., `http://192.168.x.x`) to access the CUBE OS onboarding interface.
+ The first time, you’ll be prompted to set a password and timezone.

