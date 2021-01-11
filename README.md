# domoticz.functions
Script for Domoticz that allows you to create a virtual device with a value as a function of another devices' values. Like the average temperature of three termometers or the sum of five power meters

<h2>Install:</h2>
<ul>
  <li>Open the script using any text editor and copy all the text to a clipboard (CTRL-A CTRL-C)</li>
  <li>Open Domoticz setup, select "More options" and "Events".</li>
  <li>Click on tab [+] (Add automation script) and choose "Lua" -> "Device".
    This creates a new script with an example.</li>
  <li>Change the name to i.e. "Functions"</li>
<li>Select all the text and paste the script here (CTRL-A CTRL-V). This will replace the example text by the script.</li>
  <li>Click on Save button or use CTRL-S.</li>
</ul>  

<h2>Usage:</h2>
<ul>
  <li>Open Domoticz setup, select "Devices".</li>
<li>Find the devices you want to use with the script and write down their indexes.</li>
<li>Open Setup, select "Hardware".</li>
<li>Find "Dummy switches"  - Dummy (Does nothing, use for virtual switches only) Create Virtual Sensors). If it does not exist yet, find it in the Type menu below and add it.</li>
<li>Click on the "Create Virtual Sensors" button.</li>
<li>Choose the sensor type (i.e. "temperature").</li>
<li>Give this virtual sensor a name. The name must started by the equal sign '=' followed by a name of the function and the parameter(s) between the parenthesis. The name can be modified later in Devices menu "".<br>
i.e. =AVG(10,11,12) - gives the average value (temperature) of three sensors, the devices with index 10, 11 and 12<br>
Note: no spaces are allowed</li>
</ul>
<h3>Available functions:</h3>
<ul>
<li>=MIN(a,b,c,...) - shows the value of the sensor with the smallest value</li>
<li>=MAX(a,b,c,...) - shows the value of the sensor with the maximum value</li>
<li>=AVG(a,b,c,...) - shows the average value of all the sensors given</li>
<li>=SUM(a,b,c,...) - shows a summary of all the values of the sensors given</li>
</ul>
A number of parameters is variable
