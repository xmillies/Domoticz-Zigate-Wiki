## Overview

The purpose is to give you a cookbook to pair Schneider Wiser devices to Zigate and the Domoticz plugin.

## Domoticz - initial setup

If not yet done, you have to create a plugin instance in domoticz for the Zigate hardware ( USB, DIN, PiZigate)

1. go in domoticz->setup->hardware
1.  Create the hardware device in domoticz of type "zigate plugin"
1. select the correct type of zigate and its connection details.
<br />

## Zigate admin - wiser specfic config

There are 2 important parameters/settings to be addressed in order to get the devices correctly paired and functional with the Zigate environment.

* Channel: We have tested the Schneider Wiser devices on channels 11 and 15.
* ExtendedPANId: The Schneider Wiser seem to be supported on a particular range of ExtendedPANId ( Zigbee network ). For now that is the only brand we have seen this needs and from our experience is compatible with other brands like Ikea, Philips, Xiaomi, Tuya ...

1. go in http://[domoticz_server_hostname]:[default)port _is_9440]/settings
1. select "settings" in the top bar
1. put the toggle "Advanced settings" to ON
1. find the menu zigate settings and you should find "zigate channel" and "extendedPANID" under it
1. for zigate channel , select 15 or 11
1. for extendedPANID, select a numer between 1000 and FFFF and concatenate 484504015e10
eg : randomly select 2141, your extendedPANID will be 2141484504015e10
1. enable the parameter in  Schneider Wiser settings called enableSchneiderWiser
1. click "Validate" at the top right
<br />

## Domoticz 

In order to get those settings in consideration you need to re-format the Zigate. It will them remove all already paired devices.

1. go back to domoticz->setup->hardware
1. Select your "zigate plugin" hardware
1. switch "Erase Persistent Data ( !!! full devices setup need !!! )" to TRUE
1. click update

<br />
1. switch "Erase Persistent Data ( !!! full devices setup need !!! )" to FALSE
