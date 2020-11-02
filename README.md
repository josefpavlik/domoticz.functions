# domoticz.functions
Script for Domoticz that allows you to create virtual device with value as function of another devices' values.
Like average temperature of three termometers or sum of five power meters

Install:
Open the script and get it in the clipboard (ctrl-A ctrl-C)
Open setup of Domoticz, select "More options", then "Events".
Click on tab [+] (Add automation script) and choose "Lua" -> "Device"
This creates new script with some example.
Change the name to i.e. "Functions"
Select all the text and do Paste (ctrl-A ctrl-V). This will replace the example text with the script.
Click on Save or make cltr-S.

Usage:
Open setup of Domoticz, select "Devices".
Find and note the indexes of devices to be source of the function.
Open setup, select "Hardware".
Find "Dummy switches"  - Dummy (Does nothing, use for virtual switches only) Create Virtual Sensors)
If it does not exists, create it.
Click on button "Create Virtual Sensors"
Choose the sensor type (i.e. "temperature") 
Give the name to this virtual sensor. The must be formed by the equal sign '=', function name and the parameter(s) between the parenthesis. The name can be modified later in the page "Devices".
i.e. =AVG(10,11,12) - gives the average value (temperature) of three sensors, devices with index 10, 11 and 12
Note, no spaces are allowed

Available functions:
=MIN()
=MAX()
=AVG()
=SUM()

