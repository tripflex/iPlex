	 d8b   8888888b. 888
	 Y8P   888   Y88b888
	       888    888888
	 888   888   d88P888 .d88b. 888  888
	 888   8888888P" 888d8P  Y8b`Y8bd8P' 
	 888   888       88888888888  X88K 
	 888   888       888Y8b.    .d8""8b. 
	 888   888       888 "Y8888 888  888   

# iPlex - Plex Install Helper

This is a bash/shell install helper script that will install the .deb file you provide the path to, and then update the init.d script.  I created this to use whenever installing or upgrading my OpenMediaVault server.  The normal Debian installer attempts to use upstart which ends up resulting in a blank plexmediaserver file in /etc/init.d.  I commonly install the latest beta releases and I may add functionality to this later to automatically check and download beta releases.

## Installation
``` bash
wget https://raw.github.com/tripflex/iPlex/master/iplex
```
## Usage
Just feed iplex the path to the plexmediaserver deb file you downloaded from Plex.
``` bash
sh iplex plexmediaserver_0.9.9.9.deb
```

## Init Script Usage
Using this should be just the same as you normally do, but as example

``` bash
/etc/init.d/plexmediaserver {start|stop|restart|status}
```

If you upgrade plex using the deb, the installer will rename the file to something like plexmediaserver.bkup, you will just need to remove the new /etc/init.d/plexmediaserver it created (should be blank), and move the backup back to it's original name.

Profit!
