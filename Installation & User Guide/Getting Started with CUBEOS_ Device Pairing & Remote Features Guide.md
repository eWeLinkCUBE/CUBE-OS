# Zigbee
Here's a full guide to adding Zigbee devices to your CUBE setup.

## <font style="color:rgb(34, 34, 34);">Prerequisites</font>
<font style="color:rgb(34, 34, 34);">Supported Zigbee dongles:</font>

+ <font style="color:rgb(34, 34, 34);">Sonoff ZBDongle-E (</font>**<font style="color:rgb(34, 34, 34);">recommended</font>**<font style="color:rgb(34, 34, 34);">)</font>
+ [<font style="color:rgb(0, 136, 204);">Others listed</font>](https://darkxst.github.io/silabs-firmware-builder/)<font style="color:rgb(34, 34, 34);"> by developer </font>[<font style="color:rgb(34, 34, 34);">@darkxst</font>](https://forum.ewelink.cc/u/darkxst)

<font style="color:rgb(34, 34, 34);">Supported Zigbee clusters:</font>

+ [<font style="color:rgb(0, 136, 204);">cube-web.ewelink.cc</font>](https://cube-web.ewelink.cc/)

## **Install Zigbee Adapters**
Before adding a Zigbee device, you need a Zigbee adapter, typically a USB dongle. Insert the Zigbee adapter into the USB port of the device running CUBE OS.

+ **Raspberry Pi**

Plug your Zigbee Dongle into a USB port.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750237834194-648aece5-14f6-43a5-ad5a-19e7665724f3.png)

+ **Virtual Machine(Generic)**

Insert your Zigbee Dongle on your host device and select the correct controller type under "**USB**". In the USB filter, add the necessary Zigbee Dongle using the add button on the side.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750238098349-e6ac2ce1-b4fa-469b-95f9-2b7d11800263.png)

+ **NAS**

Plug in your Zigbee dongle to your NAS, and pass through the device to the virtual machine on this page. 

⚠️ NAS configurations may vary depending on the brand and model you are using. Please refer to your NAS manufacturer's documentation for instructions on how to pass through USB devices to virtual machines.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750239064996-d21a26e2-10b1-4337-b265-e25e9725b619.png)

## **Initialize Zigbee**
1. To add a device, click the "**Add Device**" button on the device's homepage.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750400894060-d17d768b-8cb9-4db0-8af0-d85c58e4cf7d.png)

2. **Start Setup**, and select "**Continue**" in the pop-up window to automatically detect your inserted Zigbee adapter. 

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750400923343-50b4308a-a2fe-4043-aae1-dc6d79103c40.png)

3. Once the adapter is automatically discovered, select the Zigbee adapter you wish to use from the list and click "**Confirm**" to complete the configuration.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750400967431-ff232847-74a8-4ef8-a8b7-6f6bab711ec5.png)![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750401128931-e5324cdd-7249-4796-a02c-9d03c713a32b.png)

4. If your Zigbee adapter is not detected, you may **manually** add it by inputting the necessary information:
+ **Serial Path**: Check the "All Hardware" section on the settings page for the serial port path of the inserted Zigbee adapter.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750401204519-fcaa1b75-109e-4c5d-9ff5-a56f1bf8173b.png)

+ **Protocol Stack Type**: Currently supports EZSP, Deconz, ZStack, and Zigate. Check the adapter's purchase site for the corresponding protocol stack type.
+ **Port Speed**: Optional, not applicable to all Zigbee adapters.
+ **Data Flow**: Optional, not applicable to all Zigbee adapters.
5. Submit the configuration by clicking confirm. If successful, you can add Zigbee devices. In case of a failure, check the specific error message.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750401304900-01164bb4-d79e-4f72-a942-0a99ea41e851.png)

 ⚠️  Since a Zigbee network can only have one adapter configuration, multiple setups are not supported. If a configured adapter is removed and then reinserted, it will attempt to automatically restore itself without needing reconfiguration.

## **Add Zigbee Devices**
1. After configuration, on the add device page, click "**Start Setup**" to add Zigbee devices in pairing mode automatically. If your Zigbee device is not found, ensure the device is in network configuration mode and check for excessive surrounding radio interference.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750401547545-026c3417-3a0f-4565-b815-d1875c46347f.png)

2. Discovered Zigbee devices will be then added to your CUBE OS, ready to assign a room or edit name.

# Matter
A guide to add Matter devices to CUBE OS. You can also share Matter devices from other apps following the provided steps.

## <font style="color:rgb(34, 34, 34);">Prerequisites</font>
 eWeLink CUBE OS includes a built-in **Matter Hub (Controller)** that allows you to pair and control Matter-compatible devices locally.  

 To check which Matter devices are supported, please refer to the Supported Accessories [List](https://forum.ewelink.cc/t/ewelink-cube-matter-hub-compatibility/78282).  

## Find the Matter Onboarding Code
1. Look for the Matter onboarding code on your device's label, packaging, or user manual. It looks similar to this:

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750401902634-4b81de88-ba26-42eb-9e99-e49b954009e0.png)

 ⚠️  Some products (e.g., older Wiz plugs or Matter Bridges) require pairing with their official app first to generate the onboarding code. Please consult the manufacturer's instructions.

## Start Pairing with CUBE OS
1. Open your CUBE OS dashboard.
2. Click the **Add Device** button.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750402096362-84ddabb1-41f9-49df-b73d-3ac7995af77f.png)

3. Power on your Matter device and enable pairing mode (refer to manufacturer's guide).
4. Click **Start Setup**.

CUBE OS will automatically scan for devices in pairing mode.

## Choose Setup Mode
1. Auto Mode

Select the device from the available list and proceed.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750402899387-e16ae4cc-5c35-4986-a1c9-033b8b7c5588.png)

2. Manual Mode

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750402934634-a7e35234-725a-4a05-a278-63112a7ae0d6.png)

+ Enter the onboarding code from Step 1.
+ If prompted, enter your Wi-Fi credentials.
+ Click **Next** to start the pairing process.
+ Once completed, you'll be asked to name your device and assign it to a room.

# Remote Access & Notifications 
## Prerequisites
eWeLink CUBE OS provides a **Remote Features** option that lets you:

+ Access your CUBE OS web console remotely
+ Use eWeLink CUBE CAST dashboards outside your LAN
+ Receive push notifications (via browser)

⚠️ Make sure your CUBE OS device is connected to the internet. These features rely on WAN access.

## Enable Remote Features
1. Open the **CUBE OS web interface** in your browser.
2. Navigate to **Pilot Features > Remote Features**.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750403668109-d442a2ad-bfec-4eba-baa4-056e2056ca91.png)

3. Toggle the switch to enable Remote Features.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750404052451-57cc01dd-bccf-46be-a023-af2905287881.png)

Once enabled, CUBE OS will generate:

+ A remote web access link to your CUBE OS Web
+ A separate CAST dashboard link

Copy and save these links securely. Keep your PIN confidential.

## Setup eWeLink CUBE CAST on Your Phone
#### 3.1 Open the CAST Link
1. Copy the CAST link generated above.
2. Paste it into your mobile browser (Safari or Chrome are recommended).

![](https://cdn.nlark.com/yuque/0/2025/jpeg/55334511/1750405430387-f3455c0e-6a16-4590-8625-05cec8e4e719.jpeg)

#### 3.2 Add CAST to Home Screen
+ **Safari**:
    1. Tap the **Share** icon in the center of the bottom tab bar.
    2. Select **Add to Home Screen**.
+ **Chrome**:
    1. Tap the **⋮ menu** next to the address bar.
    2. Select **Add to Home Screen** or **Install App** if prompted.

![](https://cdn.nlark.com/yuque/0/2025/jpeg/55334511/1750405476205-a5c1b2c4-0615-43e6-bc5b-2720efff3a0c.jpeg)![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1750405300878-079f87d4-8213-4c7a-b864-c6de413fa501.png)

After this step, a CAST icon will appear on your home screen like a regular app.

## Enable Notifications
1. Tap the CAST app icon from your home screen to launch.
2. If prompted for permission, tap **Allow Notifications**.

⚠️ If no prompt appears, tap the **Alarm icon**, then click the banner that says _"No notifications without system permission"_. This action will trigger the system prompt again.

![](https://cdn.nlark.com/yuque/0/2025/jpeg/55334511/1750406369090-fb5b5548-0faa-4c89-a14a-4b6dd5f2d934.jpeg)![](https://cdn.nlark.com/yuque/0/2025/jpeg/55334511/1750405813397-dd91c2cc-4500-4976-9a6c-d8cf108cb15c.jpeg)

Once permission is granted, CAST will start delivering notifications such as:

+ **Security alerts**
+ **Device state changes**
+ **Automation trigger reports**
+ **Battery warnings**

## Notes & Compatibility
+ Remote Access is  **PWA browser-based**, and feature support depends on:
    - Your phone's **OS version**
    - The **browser** you use
+ For the best experience, use the **latest Safari or Chrome** on mobile.
+ PIN protection helps keep remote access secure — do not share it publicly.

