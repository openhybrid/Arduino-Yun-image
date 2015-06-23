# Installation on an Arduino Yun

Prepare the micro SD Card
-------------------------

This tutorial works with linux and osx.

You need:

- A new Arduino Yun wiht Firmware 1.4+

- Micro SD Card with a minimum of 500mb 

- Personal Wifi Network. (If Services like Airplay work, Hybrid Objects should work). 


Download and unzip the Arduino Yun Image to your computer.
You will now have a folder with the hybrid.dmg image on your computer.

Within the terminal, open the folder that stores the hybrid.dmg file.
 
With a microSD to SD Card adapter, plug your micro SD Card in your computer.

Type in the followitng into the terminal:
 
		diskutil list
 
You will see all the disks that are mounted in your computer.
Find the one disk that has the capacity of your own SD card.
For example the name could be "/dev/disk2"

Now type in the terminal:

		diskutil unmountDisk [your SDCard Name]
 
!!Make sure that you know the name of your SD Card. If you use the name of another disk connected to your computer, you will overwrite the data on this disk!!

All previously stored data on the SD Card will be lost after the following step!!!!
 
Once the SD Card is unmounted, clone the image file to the SD Card.
 
You can do this step with the following command:
 
		sudo dd if=hybrid.dmg of=[your SDCard Name]
 
The Terminal will ask for your password.
Once you have started the process, it can take a few minutes until the terminal responds again.

You have now successfully prepared the SD Card for your Hybrid Object.
 
 
Reset your Arduino
Now plug the mini SDCard into your Arduino and power it up. 

Once the white LED on your Arduino glows, you will find an open WIFI named Arduino followed by some numbers.
 
Connect to this network.
 
Open the following page in a web-browser:
 
arduino.local
 
You will be asked for a password, which is "arduino".
 
Now go to the bottom of the page and push the reset button.
 
 
Once the Arduino has reset, your Arduino is a Hybrid Object.
 
Congratulations!
 
Make sure that your computer, iOS-Device and Arduino Yun are in the same private local Network.
Cooperate Networks are not supported.
 
Now follow the Tutorial on the Use page. 