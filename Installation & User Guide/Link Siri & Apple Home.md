

This guide shows you how to bring your **eWeLink LAN devices** into CUBE OS via the **eWeLink Smart Home Add-on**, and then link them to **Apple Home** through the built-in Matter Bridge, so you can control them with **Siri**.

# Add eWeLink LAN Devices to CUBE OS
## Requirements
+ Enough storage to install Docker and volumes.
+ Internet access.

## Access Docker Tab
1. Visit **CUBE OS** via browser:
    - [http://cube.local/](http://cube.local/)
2. Click on the **Docker** tab.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1756200353403-43166ebc-3e35-4c37-844f-92e5e9e7462b.png)

## Install eWeLink Smart Home Add-on
1. Find the item named **eWeLink Smart Home**.
2. Click **Install** and wait until it finishes downloading.
3. On the Add-on card, click **Run** (leave configurations unchanged).

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1756200403741-bf983847-8cd6-4e4b-85d6-ae1494e2f4c4.png)

## Authorize
1. Once the Add-on loads up, it will **discover eWeLink-supported LAN devices** automatically.
2. Click the **login icon** in the top-right corner to sign in with your eWeLink account.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1756200464474-595b2219-8f4e-4e49-947a-1cdb07c36f9f.png)

3. Click the **Sync** button on any device → CUBE OS will issue a token → click **Allow** in the pop-up.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1756200522457-fe191b19-c7ee-400b-9235-e8ba371ff62d.png)

## Sync Devices
1. To sync devices into your CUBE OS setup, click the **Sync** button on desired devices.
2. Go to the **All Devices** tab to view the newly synced devices.
3. Assign rooms and edit device names as needed.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1756200628778-b52b05dc-1d25-4732-be0c-21fbd49885b7.png)

# Enable Matter Bridge in CUBE OS
1. In the CUBE OS web UI, click the **Matter** logo in the side panel.
2. Follow the guide to enable the feature.
3. A **QR Code** and **numeric setup code** will be displayed.

![](https://cdn.nlark.com/yuque/0/2025/png/55334511/1756191031304-c42a48af-7543-4aff-b63c-db7cbc7fbd69.png)

# Add Devices to Apple Home
## Scan QR Code
1. Open the **Camera** app on your iPhone or iPad.
2. Scan the QR Code displayed by CUBE OS.
3. Tap the **yellow banner “Open in Home”**.

<img src="https://cdn.nlark.com/yuque/0/2025/png/55334511/1756191056816-8cab26fc-8dab-45cc-80bd-a656fc44f065.png" width="250">

## Configure in Apple Home
1. iOS/iPadOS will redirect you to the **Apple Home** app.
2. Rename devices and assign them to rooms.

<img src="https://cdn.nlark.com/yuque/0/2025/png/55334511/1756191096952-7f2c396a-4597-4b0d-8abb-77e712049d87.png" width="250">

## Test with Siri
Once setup is done, try commands such as:  
_“Hey Siri, turn on the living room light.”_

<img src="https://cdn.nlark.com/yuque/0/2025/png/55334511/1756191179361-224632e8-f2e1-40a1-b07c-e7fb00668323.png" width="250">

# Secondary Setup (Sharing Devices from Another Platform)
If you already linked devices with another Matter-enabled platform, you can still pair them with CUBE OS.

1. Open the **Home app** and select the device tile.
2. Open the **device control panel** → tap the **gear icon**.
3. Scroll down to **Bridge** → tap it.
4. In bridge settings, scroll to the bottom → tap **“Turn On Pairing Mode.”**
5. Copy the generated code and follow the pairing guide on the **CUBE OS** Matter page.

![](https://cdn.nlark.com/yuque/0/2025/jpeg/55334511/1756191336210-d9ae8e1f-7c23-401d-8c09-b078657b7408.jpeg)

⚠️ **Note:** This will bring **all supported devices** attached to that bridge into CUBE OS.





