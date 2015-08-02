# Installation on an Arduino Yún

## Prepare the microSD Card

This tutorial works with GNU/Linux and Mac OS X.

You need:

- A new Arduino Yún with firmware 1.4+
- MicroSD Card with at least 500 MB free space
- Personal Wifi network supporting mDNS (if services like Airplay work, Hybrid Objects should work).


Download and unzip the Arduino Yún Image to your computer.
You will now have a folder with the hybrid.dmg image on your computer.

Within the terminal, open the folder that stores the hybrid.dmg file.

### Find the SD card device

With a microSD to SD card adapter, plug your microSD card in your computer.

Type in the following into the terminal:
 
		diskutil list
 
You will see all the disks that are mounted in your computer.
Find the disk that has the capacity of your SD card.
For example the device name could be "/dev/disk2."

### Unmount the SD card device

Now type in the terminal:

		diskutil unmountDisk [your SD card device]
 
> :warning: **Warning:**  Ensure that you use the device name of your SD card. If you use the name of another 
disk connected to your computer, you will overwrite the data on this disk!  All previously 
stored data on the SD card will be lost after the image is written.
 
### Clone the image file to the SD card
 
You can do this step with the following command:
 
		sudo dd if=hybrid.dmg of=[your SD card device]

If prompted for your password, enter it.  Once you have started the process, it 
can take a few minutes until the terminal prompt returns.

> **Note:**  In Mac OS X each disk may have two path references in /dev:
* `/dev/disk#` is a buffered device, which means that data being sent to it undergoes extra processing
* `/dev/*r*disk#` is a _raw_ device, which is much faster and compatible with the dd utility

You have now successfully prepared the SD card for your Hybrid Object.
 
 
## Boot from SD card and reset your Arduino

Plug the microSD card into your Arduino and power it up.  Once the white LED on your Arduino glows, 
you will find an open WiFi network named "Arduino" followed by some numbers.
Connect to this network.
 
Open the following page in a web-browser:
 
    http://arduino.local
 
You will be asked for a password, which is "*arduino*."
 
Now go to the bottom of the page and push the reset button.
 
 
Once the Arduino has reset, your Arduino is a Hybrid Object.
 
**Congratulations!**
 
If you have trouble, make sure that your computer, iOS device, and Arduino Yún are in the same
private local network. Corporate networks are not supported.
 
Now follow the tutorial on the "Use" page. 
