#Ubuntu
## Problem: Downloads of packages very slow or repo server is down

### Solution
Go to Ubuntu Software Center
Edit-> Software Resources -> Download From -> Choose Other
Click Select Best Server
Wait until it finished and when finished, the best server is the selected
Finally just press Choose Server

### Problem: Started installing/downloading something using apt-get install, but you changed your mind and want to cancel it.

### Solution

If you press Control+C it could generate a improper installation.

Kill the process named apt-get:

killall -9 apt-get

Reconfigure dpkg:

dpkg --configure -a

Update apt-get:

apt-get update

Update packages, including those improperly installed:

apt-get upgrade


## Problem: You want to know what's happening exactly in your system

### Solution
Check logs at: `/var/log/syslog` and `/var/log/kern.log`
