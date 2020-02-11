In Domoticz, go in domoticz->setup->hardware
*  Create the hardware device in domoticz of type "zigate plugin"
*select the correct type of zigate and its connection details.


* go in http://[domoticz_server_hostname]:[defalut)port _is_9440]/settings
* select "settings" in the top bar
* put the toggle "Advanced settings" to ON
* find the menu zigate settings and you should find "zigate channel" and "extendedPANID" under it
* for zigate channel , select 15
* for extendedPANID, select a numer between 1000 and FFFF and concatenate 484504015e10
eg : randomly select 2141, your extendedPANID will be 2141484504015e10


* go back to domoticz->setup->hardware
* Select your "zigate plugin" hardware
* switch "Erase Persistent Data ( !!! full devices setup need !!! )" to TRUE
* click update

* switch "Erase Persistent Data ( !!! full devices setup need !!! )" to FALSE
