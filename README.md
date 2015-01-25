# ESP8266-WiFi-HotSpot-Locater
ESP8266 Gizmo to connect to the strongest open Hotspot

More information at http://benlo.com/esp8266/esp8266Projects.html#hotspotfinder

<h3>Open Hotspot finder</h3>
<p>
My goal was to create a simple hand held hot spot locator, which would quickly tell me
if I can connect to one of the several WiFi routers around our home from any given
location. If this works, then I can create other IoT gizmos that automatically seek out
the strongest signal and connect to them automatically. My WiFi access points do not
require a password.
</p>
<p>
In most cases, the use of a device like this to connect to a WiFi hotspot requires the authorization
of the owner of the access point. Please only use this code to access hotspots which you are already
authorized to use.
</p>
<p>
No connections are needed to the board, other than the usual TXD, RXD and ground for programming.
This board comes with the battery already wired.
</p>
<p>
When power is applied to the board, the program searches for access points that are in range and
chooses the strongest one that is open and does not require a password to connect. If it finds any open access points
in range, the LED changes from RED to BLUE.
</p>
<p>
Hotspot finder then attempts to connect to the access point and, once connected, it
sends a query to a php script on a web site. 
If the expected response is received, the LED changes from BLUE to GREEN.
</p>
<p>
If a response is received, but it does not match the expected response, it indicates
that there may be an additional login required, or the access point is not connected to the internet,
and the LED changes to PURPLE.
</p>
<p>
After 5 seconds, the LED goes off. If power is left on, the finder tries again in 
30 seconds.
</p>
<p>
Experimentation has shown that a connection can be established and verified in less than 3 seconds.
</p>
