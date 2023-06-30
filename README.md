# traccar_device_online
![alt text](https://raw.githubusercontent.com/unix1984/traccar_device_online/main/img/traccar_devices_online.png)
This is a simple BASH script to check the online status of Traccar devices with Nagios.
<br/>
You must enter the time in seconds, which must not be exceeded. If the "-t" value of t is 600, then the GPS Tracker has not sent a signal for 10 minutes and nagios will indicate it.
<br/>
How to use:
```
~]$ /usr/lib/nagios/plugins/check_traccar_device_online -i 7501043656 -t 600 -l /mnt/sda3/containers/alpine-gps/rootfs/opt/traccar/logs/tracker-server.log
OK - Device 7501043656 is online
```
<br/>
<br/>
**Install:**

```wget -O /usr/lib/nagios/plugins/check_traccar_device_online https://raw.githubusercontent.com/unix1984/traccar_device_online/main/check_traccar_device_online && chmod  +x /usr/lib/nagios/plugins/check_traccar_device_online```
