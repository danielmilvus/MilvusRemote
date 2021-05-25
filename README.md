# MilvusRemote
Remote access solution
Windows:
	1. Clone MilvusRemote 'https://github.com/danielmilvus/MilvusRemote'
	2. cd MilvusRemote
	3. Make guaca-install.sh exec. (sudo chmod +x guaca-install.sh)
	4. To run the script: (REPEATER: If you don´t want to install it, use --repeater false)
		./guaca-install.sh --mysqlpwd password --guacpwd password
	5. Test guac server:
		http://Server:8080/guacamole
		User: guacadmin 
		Pwd:  guacadmin
	6. Test repeater:
		run: sudo lsof -i -P -n
		Check if the uvncrepeater is running and listening ports 5901 and 5500.
Linux:
	1. If your distro is using Wayland, you must disable it:
		https://linuxconfig.org/how-to-disable-wayland-and-enable-xorg-display-server-on-ubuntu-18-04-bionic-beaver-linux
	2. Install x11vnc: 
		sudo apt-get update
		sudo apt-get install x11vnc
	3. Create a password:
		x11vnc -storepasswd
	4. Connect:
		x11vnc -connect repeater=ID:123+54.232.251.221:5500
