# SquidScripts
Automation Scripts for "Squid for Windows" proxy
a list of batch files, for easy install and Conifguration of Squid proxy, including:
 - creating shortcut in startup for the Squid System Tray Icon
 - selecting your Squid ACLs and Rules from predefined blocklists (Block windows update, Block Telemetry, both, or none)
 - setting WinHTTP API to use Squid proxy 
 - setting WinINET to use Squid proxy 
 - setting System Environment Variables HTTP_PROXY and HTTPS_PROXY to point to Squid Proxy
 - Copies the "RunAtStartup.bat" into the Squid Directory (where ever it was installed) 
 - Copies the "Proxy_Disable.bat" into the Squid Directory (where ever it was installed) 
 - Copies the "Proxy_Enable.bat" into the Squid Directory (where ever it was installed) 
 - Copies the "Proxy_Show.bat" into the Squid Directory (where ever it was installed) 
 - Creates shortcuts to Start Menu for Proxy Disable / Enable / Show scripts 
 - Creates Scheduled Task on startup, that enforces WinHTTP / WinINET / EnvVar settings, and Squid Proxy

Firstly, to Install Squid for Windows Proxy, download from their website:

Website:
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
https://packages.diladele.com
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

PLEASE NOTE:
Specifically download "Squid for Windows" MSI
NOT the Web Proxy for Windows...thats something else entirely. 

Direct Download of Version 4.14 -(correct as of 20/10/2024)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
https://packages.diladele.com/squid/4.14/squid.msi
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
(otherwise, get the latest from the main site) 


Secondly, download the "SquidScripts" from this repository 
copy the entire squid Scripts folder somewhere on your machine. 
or keep them in the root of your Squid Install Dir, doesnt matter. 
but keep them in the SAME STRUCTURE they're in!!
(the installConfig.bat file expects certain files in certain places)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Just Run the "InstallConfig.bat" as ADMIN
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
