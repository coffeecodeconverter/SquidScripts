Squid For Windows (Proxy Server) 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
https://github.com/diladele/squid-windows
https://packages.diladele.com
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


# SquidScripts
Automation Scripts for "Squid for Windows" proxy


The purpose is to make configuring Squid for Windows as easy as possible. 
Because running the MSI just installs the service (squidsrv), sets it to automatic, and thats it. 


You still need to (ideally) put a shortcut to the Squid System tray icon in startup.
You need to make sure the WinHTTP stack and WinINET are both using the proxy - default is 127.0.0.1:3128 
You then also need to configure your ACL's and block Rules. 
and then restart the service to pick up the changes.
thats BARE minimum to get it actually "working" instead of just "installed and running" 


thats where these SquidScripts Come in. 


It goes much further, and creates easy ways to fully enable, disable, enforce, and configure squid in seconds. 


A list of batch files, for easy install and Configuration of Squid proxy, including:
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

includes 4 x preconfigured Squid.conf files:
- Block Windows Update
- Block Windows Telemetry
- Block Both
- Block Nothing (essentially, same as a default squid.conf)

you can edit the InstallScript.bat if you want, to add more options
and then add a corresponding squid.conf to the "_Configs\" folder that comes with the SquidScripts. 

When using InstallConfig.bat to select a block list, 
It backs up any existing squid.conf with a timestamp, so you never lose a one by mistake. 
It finds the install directory by checking the "squidsrv" service binPath, 
and uses relative pathing from there to get to your Squid\etc\squid\squid.conf File.
then restarts the service to pick up the changes. 



INSTALL SQUID
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





DOWNLOAD SQUID SCRIPTS
Secondly, download the "SquidScripts" from this repository 


copy the entire squid Scripts folder somewhere on your machine. 
or keep them in the root of your Squid Install Dir, doesnt matter. 


but keep them in the SAME STRUCTURE they're in!!

(the installConfig.bat file expects certain files in certain places)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Just Run the "InstallConfig.bat" as ADMIN
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you're worried about running some random batch file from the internet as admin, i assure you, this does only and exactly whats it says on the Tin. 


but, you can always:
- run in a VM first
- Paste it into chatGPT / claude / Gemini / CoPilot / ANY ai you can think of and get it to verify for you for speed.
- open the scripts in notepad and check them yourself.


  i created these to make it easier for myself, given the numerous extra little steps you have to do.

  and thought, why not share it with the world.

  simple as that

  
