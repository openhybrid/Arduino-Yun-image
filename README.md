# Installation on an Arduino Yún

## Prepare the microSD Card

This tutorial works with GNU/Linux and Mac OS X.

You need:

- A new Arduino Yún with firmware 1.4+
- MicroSD Card with at least 500 MB free space
- Personal Wifi network supporting mDNS (if services like Airplay work, Hybrid Objects should work).


Download and unzip the Arduino Yún Image to your computer.
You will now have a folder with the `hybrid.dmg` image file on your computer.
Using the terminal (command line), navigate to the folder containing the `hybrid.dmg` file.

### Find the SD card device

With a microSD to SD card adapter, plug your microSD card in your computer.
Enter the following command into the terminal:

**Mac OS X**

    diskutil list

**Linux**

    sudo fdisk -l
 
You will see all the disks that connected to your computer.
Find the device name for the disk that has the capacity of your SD card.
For example the device name could be "/dev/disk2" or "/dev/mmcblk0."

### Unmount the SD card device

**Mac OS X**

    diskutil unmountDisk [your SD card device]

**Linux**

    sudo umount [your SD card device such as /dev/mmcbkl0]
 
> :warning: **Warning:**  Ensure that you use the correct device name for your SD card. If you use the name of another 
disk connected to your computer, you will overwrite the data on this disk!  All previously 
stored data on the SD card will be lost after the image is written.
 
### Transfer the image file contents to the SD card device
 
Enter the following command, replacing "[your SD card device]" as appropriate for your SD card's device name:
 
    sudo dd if=hybrid.dmg of=[your SD card device]

Enter your password if prompted.  It can take several minutes until the transfer completes and the 
terminal prompt returns.

You have now successfully prepared the SD card for your Hybrid Object.  Remove the SD card from the computer.
 
## Boot from SD card and reset your Arduino

Plug the microSD card into your Arduino and power it up.  Once the white LED on your Arduino glows, 
you will find an open WiFi network named "Arduino" followed by some numbers.
Connect to this network.
 
Open the following page in a web-browser:
 
    http://arduino.local
 
Use password "arduino" when prompted.  Scroll to the bottom of the page and push the reset button.
 
Once the Arduino has reset, your Arduino is a Hybrid Object.
 
**Congratulations!**
 
If you have trouble, make sure that your computer, iOS device, and Arduino Yún are in the same
private local network. Corporate networks are not supported.
 
Now follow the tutorial on the "Use" page. 
