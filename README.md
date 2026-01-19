# bleshark-nano-eu-firmware-guide
Step-by-step guide for installing EU firmware on the BLEShark Nano

# Introduction
Starting August 1, 2025, new EU regulations under the Radio Equipment Directive (RED) restrict certain Wi-Fi functions. As a result, the BLEShark Nano EU firmware no longer includes the Deauth option.

This guide demonstrates how to configure a hotspot with a USA VPN to allow installation of the USA firmware, which retains the Deauth functionality.

Disclaimer: This guide is provided “as is”. It comes without any warranty and is not supported or endorsed by InfiShark Tech. Use it at your own risk.

***Note: Some images in this guide have been partially edited or cropped to protect privacy.***

# For Windows 11 Users

**1. Download and install OpenVPN Connect for Windows from the following link:**
* https://openvpn.net/client/

**2. Open the Network Adapter settings:**
*	Go to Control Panel → Network and Internet → Network and Sharing Center.
*	Click Change adapter settings.
*	You should see the TAP adapter, as shown in the image below.

![Image](https://github.com/IkerGarcia/bleshark-nano-eu-firmware-guide/blob/main/pictures/1.png)
 
**3. Download an OpenVPN profile for the USA.**
*	In most cases, any country outside the EU will work, but using a USA profile is recommended to avoid potential issues.

**4. Launch OpenVPN Connect:**
*	Select Upload File, as shown in the image below.
*	Once the profile is loaded, click Connect.

 ![Image](https://github.com/IkerGarcia/bleshark-nano-eu-firmware-guide/blob/main/pictures/2.png)
 
**5. Verify your IP address:**
*	Visit https://whatismyipaddress.com/.
* Confirm that your IP address location is shown as United States (USA).

![Image](https://github.com/IkerGarcia/bleshark-nano-eu-firmware-guide/blob/main/pictures/3.png)
 
**6. Configure the Mobile Hotspot settings:**
*	Go to Settings → Network & Internet → Mobile hotspot.
*	Select Edit and set the Network band to 2.4 GHz (mandatory).
*	Optionally, change the network name and password as desired.

![Image](https://github.com/IkerGarcia/bleshark-nano-eu-firmware-guide/blob/main/pictures/4.png)
 
**7. Return to Network Adapter settings:**
*	Go to Control Panel → Network and Internet → Network and Sharing Center.
*	Click Change adapter settings.
*	You should now see a new adapter named Microsoft Wi-Fi Direct Virtual Adapter.

![Image](https://github.com/IkerGarcia/bleshark-nano-eu-firmware-guide/blob/main/pictures/5.png)

**8. Enable Internet sharing on the OpenVPN adapter:**
*	In the same window, locate TAP-Windows Adapter V9 for OpenVPN (from Step 2, Picture 1).
*	Right-click the adapter and select Properties.
*	Open the Sharing tab.
*	From the dropdown menu, select the adapter that corresponds to Microsoft Wi-Fi Direct Virtual Adapter.
*	Enable Internet Connection Sharing, then apply the changes.

***Note: the system language was not changed in this menu in my computer.***

![Image](https://github.com/IkerGarcia/bleshark-nano-eu-firmware-guide/blob/main/pictures/6.png)
 
**9. (Optional) Connect a device to the hotspot:**
*	Connect any device to the newly created hotspot.
*	Go back to Settings → Network & Internet → Mobile hotspot.
*	Verify that the connected device is listed as Connected.

![Image](https://github.com/IkerGarcia/bleshark-nano-eu-firmware-guide/blob/main/pictures/7.png)
 
**10. (Optional) Verify the VPN on the connected device:**
*	On the device connected to the hotspot, visit https://whatismyipaddress.com/.
*	Confirm that the IP address location shows United States (USA), indicating that the VPN is properly shared through the hotspot.
*	It should match the IP displayed in Step 5 / Picture 3.

**11. Connect to the BLEShark Nano hotspot:**
*	Open a browser and go to https://docs.infishark.com/docs/basics/getting-started.
*	Follow the instructions on the page to connect to the BLEShark Nano hotspot.
*	Note: The phone’s SIM card was disconnected to prevent any non-USA IP from showing. The phone is not connected to the VPN hotspot, it only connects directly to the Nano.

**12. Select your Windows hotspot in BLEShark Nano:**
*	On the BLEShark Nano configuration page, choose the SSID of your Windows hotspot that you set up in Step 6.

**13. Verify successful configuration:**
*	Once the initial configuration is complete, the Deauth option should appear in the Wi Fi menu.

# Contributors

Everyone can contribute to this project, improving the text or adding different OS.


