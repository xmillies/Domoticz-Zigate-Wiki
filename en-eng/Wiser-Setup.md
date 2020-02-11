Domoticz - initial setup
* go in domoticz->setup->hardware
*  Create the hardware device in domoticz of type "zigate plugin"
* select the correct type of zigate and its connection details.
<br />

Zigate admin - wiser specfic config
* go in http://[domoticz_server_hostname]:[defalut)port _is_9440]/settings
* select "settings" in the top bar
* put the toggle "Advanced settings" to ON
* find the menu zigate settings and you should find "zigate channel" and "extendedPANID" under it
* for zigate channel , select 15
* for extendedPANID, select a numer between 1000 and FFFF and concatenate 484504015e10
eg : randomly select 2141, your extendedPANID will be 2141484504015e10
* enable the parameter in  Schneider Wiser settings called enableSchneiderWiser
* click "Validate" at the top right
<br />

Domoticz 
* go back to domoticz->setup->hardware
* Select your "zigate plugin" hardware
* switch "Erase Persistent Data ( !!! full devices setup need !!! )" to TRUE
* click update

<br />
* switch "Erase Persistent Data ( !!! full devices setup need !!! )" to FALSE
