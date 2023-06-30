![alt text](https://raw.githubusercontent.com/unix1984/btrfsback-lite/main/img/Backup-Email-Report.png)

# traccar_device_online
This is a simple BASH script to check the online status of Traccar devices with Nagios.
<br/>
You must enter the time in seconds, which must not be exceeded. If the "-t" value of t is 600, then the GPS Tracker has not sent a signal for 10 minutes and nagios will indicate it.

How to use:
~]$ /usr/lib/nagios/plugins/check_traccar_device_online -i 7501043656 -t 600 -l /mnt/sda3/containers/alpine-gps/rootfs/opt/traccar/logs/tracker-server.log
OK - Device 7501043656 is online.
	  
![alt text](https://raw.githubusercontent.com/unix1984/btrfs/main/img/btrfsback-lite-help.png)
<br/>
<br/>
Daily E-Mail report:
![alt text](https://raw.githubusercontent.com/unix1984/btrfsback-lite/main/img/Backup-Email-Report.png)
<br/>

**Install:**
