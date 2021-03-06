# C++ Hologram SDK
Libraries to help you get connected with the Hologram Nova 

This is an unoffical repo to connect the Hologram Nova and other modems to the hologram network.

## Windows Desktop
This version makes use of the [Windows RAS component](Understanding_RAS.md "Windows RAS component") to create and dial up a connection to the cellular network.

### Uses the following static libraries:
 * rasapi32.lib
 * Cfgmgr32.lib
 * Ws2_32.lib
 
## Windows IOT Core/Windows Universal App
Currently there does not appear to be a PPP implmentation in the IoT Core so this will try to create a minimal working option. 

Possible options for a PPP stack might be found/written using: 
 * http://savannah.nongnu.org/projects/lwip/
 * https://os.mbed.com/users/nixnax/code/PPP-Blinky/

### Uses the following static libraries:
 * onecoreuap.lib
 * Cfgmgr32.lib
 * Ws2_32.lib

## MacOS
Give it a test run!

PPP hasn't been added yet so creating a data connection is not possible, but sending messages and getting SMS work

### Required Frameworks:
 * IOKit
 * Core Foundation

## Linux
While it should probably compile it has not been tested yet and our offical python SDK is a much better option for deveopers
https://github.com/hologram-io/hologram-python

PPP hasn't been added yet so creating a data connection is not possible, but sending messages and getting SMS work

### Warning 
Without routing internet traffic your machine may make a lot requests on the cellular network and cause you to rack up a lot of data usage unintentionally!

## Thanks & Credit
Some of this code was adapted from parts of the openframeworks project: https://github.com/openframeworks/openFrameworks
