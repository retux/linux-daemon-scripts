These are a set of scripts intended as tool for starting / stoping your own
daemons programs.

linux-daemon-scripts: is a skeleton script which you can customize and configure
		to fit your daemon's program needs.
	It's a sysv style init script for Debian based distros (i.e Ubuntu and others).
	This vesion use start-stop-daemon feature, and it's based on Ramesh
 Natarajan's work: http://www.thegeekstuff.com/2012/03/lsbinit-script/	

The precedure to use it with your own daemon is simple. Just have to edit

# Process name ( For display )
NAME=my-daemon
# Daemon name, where is the actual executable
DAEMON=/home/user1/my_daemon
# pid file for the daemon
PIDFILE=/var/run/my_daemon.pid	
# USER which will run the daemon
USER=myUser

Where:

NAME: is the name of your daemon program.
DAEMON: is the path to binary file.
PIDFILE: the path to pid file.
USER: is the user which will run your daemon. It's always better run a certain 
	daemon as non-privileged user.
