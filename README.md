# AmebaCloudUpdate

This update to the OTA API for the Ameba board brings in the much requested 
feature to let the board download the update from a IP:port spec.

# API
The API is pretty starghtformward to use. I have kept it close to the original library 
code design as possible

OTA.beginCloud("your IP here", OTA_PORT)

This call lets the board connect with the server via the IP:PORT specified in the
function arguments and once connected it can download the firmware from the server.

# Sample download Server

The Tools folder has a sample download server. 

* Start the server by running the script provided for Windows (start.bat)
* Make sure that you have your ota.bin file present in the root of the tools folder
* once the server starts it will wait for connection on 8082 (this and the ota file name can be changed in the start.bat file)

# Ameba example

The ota_cloud_basic example lets you take this feature for a test ride. 

* make sure you replace the OTA folder in arduino cores folder
  ** windows: Arduino15\packages\RAK\hardware\ameba\2.0.2\libraries
  ** linux ~\.Arduino15\packages\RAK\hardware\ameba\2.0.2\libraries

* Open the example .ino file in the arduino IDE (with the ameba arduino core installed)
* Change the section of the OTA API as show above.
* Also chnage your wifi SSID and password
* Run the code !!!

ota_cloud_non_block example is slightly different. The example shows how to implement the feature without 
blocking the main sys thread.

You should see the ameba board download the firmware correctly from the download server. 


