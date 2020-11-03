# domoticz.functions
Script for Domoticz that allows you to create virtual device with value as function of another devices' values.
Like average temperature of three termometers or sum of five power meters

<h2>Install:</h2>
<ul>
  <li>Open the script and get it in the clipboard (ctrl-A ctrl-C)</li>
  <li>Open setup of Domoticz, select "More options", then "Events".</li>
  <li>Click on tab [+] (Add automation script) and choose "Lua" -> "Device".
    This creates new script with some example.</li>
  <li>Change the name to i.e. "Functions"</li>
<li>Select all the text and do Paste (ctrl-A ctrl-V). This will replace the example text with the script.</li>
  <li>Click on Save or make cltr-S.</li>
</ul>  

<h2>Usage:</h2>
<ul>
  <li>Open setup of Domoticz, select "Devices".</li>
<li>Find and note the indexes of devices to be source of the function.</li>
<li>Open setup, select "Hardware".</li>
<li>Find "Dummy switches"  - Dummy (Does nothing, use for virtual switches only) Create Virtual Sensors). If it does not exists, create it.</li>
<li>Click on button "Create Virtual Sensors"</li>
<li>Choose the sensor type (i.e. "temperature")</li>
<li>Give the name to this virtual sensor. The name must be formed by the equal sign '=', function name and the parameter(s) between the parenthesis. The name can be modified later in the page "Devices".<br>
i.e. =AVG(10,11,12) - gives the average value (temperature) of three sensors, devices with index 10, 11 and 12<br>
Note, no spaces are allowed</li>
</ul>
<h3>Available functions:</h3>
<ul>
<li>=MIN(a,b,c,...) - gives the minimum value</li>
<li>=MAX(a,b,c,...) - gives the maximum value</li>
<li>=AVG(a,b,c,...) - gives the average value of sensonrs</li>
<li>=SUM(a,b,c,...) - sum values of all sensors</li>
</ul>
Number of parameters is variable
