# Description

In order for your PS3 controller to "pair" with the ESP32 you have to change your MAC address in either the controller or the ESP so that they match. I personally feel that changing the MAC on the controller is the easier method. The steps for this method are as follows:


# Files

**Ps3Address.ino** from either this repository or from the examples from the PS3_Controller_Host library on Arduino IDE.
**SixaxisPairTool** can be downloaded from [Here](https://sixaxispairtool.en.lo4d.com). This will allow you to view and edit the MAC address for your PS3 Controller


## Method
The first thing that you have to do is find out what the MAC address for your ESP32's Bluetooth is. Upload the **Ps3Address.ino** to your ESP via Arduino IDE. Once uploaded, open the Serial Monitor `Tools -> Serial Monitor` and press the boot/reset button on the ESP32. You MAC address will be displayed.

Install the **SixaxisPairTool** and run the program. It can take a few minutes the first time because it has to install the drivers. After the program is done installing the drivers, you will see that it says, "no device found".
Connect your Ps3 Controller via a USB cable to your computer and the current MAC address will be shown. Enter the MAC address for your ESP32 from the previous step into the Change Master space and press update. The Current Master should now match the ESP32's MAC address
