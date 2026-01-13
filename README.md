# Samsung-FRP-Bypass-WEB
> [!WARNING]  
> Note: This is for educational and research purposes only. Please do not use this on devices that are not your own. Data loss is likely so backup your stuff before you proceed. I am not liable for any kind of damage you cause with this tool.

With this "tool" you can bypass the FRP (Factory reset protection) on Samsung devices that have a security patch older than August 2022 (almost) entirely in your browser.

Why I say almost, is because to connect to the device you would need to have the Samsung USB driver installed, which you can download from [here](https://developer.samsung.com/android-usb-driver).

Other than that, everything happens in the browser and locally on your computer, no server-side processing.

# How to use

- Make sure you are using a chromium based browser (Chrome, Edge, Brave, Opera...)
- Make sure drivers are installed
- On your phone click "Emergency Dialer"
- Type \*#0\*# to enter "Test mode"
- When you are there, connect your device to your computer with a USB cable
- Either open the [demonstration site](https://serial.rf.gd/frp/) or run the code in this repository locally
- In the tool select "Connect" in the WebSerial section
- In the popup dialog select your device (For me its something along the lines of "CDC Abstract Control Model (ACM) (COM16)")
- After you have connected to your device, just click the buttons in order
- If you are done with that, click "Disconnect"
- Next repeat the same steps in the WebUSB section (Connect, Click buttons in order)
- If you have done everything correctly, after clicking the "Reboot" button your device should restart and you should be either on the lock screen or in the system
- On some devices you will still need to continue with the setup

#### Upadte:
An automated version is now available [here](https://serial.rf.gd/autofrp/)

# Known Issues

## Getting "The device has been lost" when sending DEBUGLVC command

### Cause:
The command "AT+DEBUGLVC" changes the USB configuration of the device, causing it to disconnect from the computer.

### Solution:
Refresh the site and reconnect to the device, after that press it again and continue with the procedure

# Credits

[WebADB](https://github.com/webadb/webadb.js/) for webadb.js 

[riskeco](https://github.com/riskeco/Samsung-FRP-Bypass) for the AT and ADB commands 
