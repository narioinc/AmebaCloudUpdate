# AmebaCloudUpdate

This update to the OTA API for the Ameba board brings in the much requested 
feature to let the board download the update from a IP:port spec.

# API
The API is pretty starghtformward to use. I have kept it close to the original library 
code design as possible

OTA.beginCloud("<your IP here>", OTA_PORT)

This call present the opportunity for the board to connect with the IP:PORT specified in the
function arguments and once connected you can download the firmware from the server.

# Sample download Server

The Tools folder has a sample download server. 

* Start the server by running the script provided for windows start.bat
* Make sure that you have your ota.bin file present in the root of the tools folder
* once the server starts it will wait for connection on 8082

# Ameba example

The ota_cloud_basic example lets you take this feature for a test ride. 

* make sure you replace the OTA folder in arduino cores folder
  ** windows: Arduino15\packages\RAK\hardware\ameba\2.0.2\libraries
  ** linux ~\.Arduino15\packages\RAK\hardware\ameba\2.0.2\libraries

* Open the example .ino file in the arduino IDE (with the ameba arduino core installed)
* Change the section of the OTA API as show above.
* Also chnage your wifi SSID and password
* Run the code !!!

You should see the ameba board download the firmware correctly from the download server. 


