via console port
	rj45 OR USB Mini-b
rollover cable
	8 pins -> 8 pins in an inverted array
		1-8, 2-7, 3-6, and so on.
terminal emulator
	PuTTy is a popular one
	change the connection type to "serial"
		configure options for the serial line in the "Serial" section of the "Connection" category
		the defaults work fine with the defaults of cisco equipment:
			9600 speed (baud (bits/s))
			8 data bits
			1 stop bit(s)
			parity = none
			flow control = none
user EXEC mode (aka user mode)
	Router>
		hostname = router, ">" = user EXEC mode
	very limited.
privileged EXEC mode
	*enable*
	Router#
	complete access BESIDES changing the config
tab completion
	*en* -> -*tab*- -> *enable*
global configuration mode
	*configure terminal* -OR- *conf t*
	Router(config)#
*enable password*
	*enable password ?* shows all possible options/parameters for *enable password* which is a plaintext pw
running-config VS startup-config
	running
		current, active configuration file
		*show running-config*
	startup
		the config loaded on restart
		*show startup-config*
*write*
	saves config
*write memory*
	saves config (same)
*copy running-config startup-config*
	pastes active config into startup config file
	saves config (same)
*service password-encryption*
	encrypts plaintext password
	must be in global config mode
	not very secure, so you must instead use:
*enable secret* {pw}
	MD5 encryption
		appears in running-config as: 
			"enable secret 5 $m%m!Rjaksndkjetcetcetc."
*no {command}*
	removes individual commands from config file
		encrypted pw's STAY encrypted
*run/do {privileged exec level command}*
	executes a privileged-exec level command from global configuration mode
