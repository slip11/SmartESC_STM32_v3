Fork of EBiCS firmware for Lishui devices. Ported to Xaiomi M365 controller. 
Use JST PA series 2mm pitch for the connectors. (need to be confirmed) 

This branch works with the original M365 dashboard  

How to use:  
Method 1 (github account needed):  
Fork the project repository to your github account by clicking the "Fork" icon.  
Edit the config.h in your repository online and commit the changes.  
Click on the "Actions" button in the menu bar of the github page. There you can see the "workflows".  
Wait until the running workflow is finished, then click on the workflow headline.
Download the zipfile with the generated zipfile by clicking on the cube icon at the bottom of the page.  

Method 2 (lokal installation):  
Install the [STM Cube IDE](https://www.st.com/en/development-tools/stm32cubeide.html#overview&secondary=st-get-software)  
Start the IDE and install egit from the eclipse marketplace (Help --> Eclipse Marketplace...)  
Import this repo from github (File --> Import --> git --> Projects from git)  

Edit the file config.h (in the folder Core/Inc) according to your wishes. Working settings for the original M365 are in the comments, so use them to have a proven start setting.  

Click on "Build" (The icon with the hammer)  

in the folder /tools/zip-output the zip-file ready for use with your scooter is generated.



Copy it to your mobile phone and flash it to the scooter by the app downG.

After flashing, lift the motor, so it can spin in the air without load. Press the dashboard button for 5s, the autodetect routine starts. The motor turns slowly. After stopping, the scooter is ready to run.  

Dashboard button use:  
short press: switch lights  
double click: switch ride modes  
long press: switch off  
very long press: run autodetect  

Caution! If you want to go back to the original firmware by OTA update, use an "old" zipfile, that contains the three files FIRM.bin FIRM.bin.enc and info.txt  With a recent zip file the controller bricks and can only flashed by a STLink afterwards.
After flashing the old original firmware you can reflash a recent version.

![PCB Layout M365](https://github.com/Koxx3/SmartESC_STM32_v3/blob/master/Documentation/PCB%20Layout%20M365.PNG)
