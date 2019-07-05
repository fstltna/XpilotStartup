# Xpilot-ng-server Startup Scripts (1.0)
Alternate startup scripts for the Xpilot-ng-server game - uses the "screen" command to manage session. This also restarts the server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/SynchronetStartup) - [Official Forum](https://synchronetbbs.org/index.php/forum/alternate-startup-scripts) 
![Synchronet Logo](https://SynchronetBBS.org/SynchronetLogo.png) 

[![Visit our IRC channel](https://kiwiirc.com/buttons/irc.synchro.net/SynchronetFans.png)](https://kiwiirc.com/client/irc.synchro.net/?nick=guest|?#SynchronetFans)

---
These start up the Xpilot server at boot time with a "screen" process.

1. Copy **xpilot** into **/etc/init.d** - make sure it is executable
2. Copy **startxpilot** into **/root/myxpilot** - make sure it is executable
3. Run "**systemctl enable xpilot**" (only needed once, will stick)
4. Run "**systemctl start xpilot**" - starts sbbs without restarting the server

When you want to view the Xpilot console, just enter "**screen -r**" in your shell.

To disconnect from the Xpilot console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/myxpilot/nostart**". To reenable it type "**rm /root/myxpilot/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
