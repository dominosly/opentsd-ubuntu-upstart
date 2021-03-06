# opentsd-ubuntu-upstart
OpenTSDB upstart script for Unbuntu 14.04  
=======
  
A simple start/stop script for OpenTSDB on Ubuntu. This was tested and used specifically on 14.04 but may work fine on other versions.  

Prerequisites
---------
An installed version of OpenTSDB: http://opentsdb.net/docs/build/html/installation.html#.  
Run 'mkdir /var/log/tsdb' or adjust the log directory to one that exists.

Installation  
-----------
Simply clone this repo and copy tsd to /etc/init.d/tsdb. Change the variable TSD_CONF to the location of your opentsdb.conf file, or ln -s your opentsd.conf file to one of the standard locations specified by the documentation: http://opentsdb.net/docs/build/html/installation.html# Now you can run 'service tsdb start'.

Details
----------
This script puts the tsd process into the background and writes both stdout and stderr to the log file specified by the variable TSD_LOG_FILE (default /var/log/tsdb/tsdb.log).
