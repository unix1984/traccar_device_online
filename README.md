# traccar_device_online
![alt text](https://raw.githubusercontent.com/unix1984/traccar_device_online/main/img/traccar_devices_online.png)
This is a simple BASH script to check the online status of Traccar devices with Nagios.
![alt text](https://raw.githubusercontent.com/unix1984/traccar_device_online/main/img/traccar_devices_nagios.png)
You must enter the time in seconds, which must not be exceeded. 
<br/>
If no entry is received from the device for the specified period of time (-t), Nagios will notify you.
<p>
<p>
<br/>
<br/>

**How to use:**

```
~]$ /usr/lib/nagios/plugins/check_traccar_device_online -i 7501043656 -t 600 -l /mnt/sda3/containers/alpine-gps/rootfs/opt/traccar/logs/tracker-server.log
OK - Device 7501043656 is online
```
<br/>
<br/>
<br/>
<br/>

```
~]$ /usr/lib/nagios/plugins/check_traccar_device_online --help

    Usage:
        -i, --identifier	-GPS tracker identifier number.
        -t, --time-interval	-GPS device data sending time interval in seconds. If this time is exceeded, it indicates offline.
        -l, --log-path          -Path to the Traccar log file.
        -h, --help		-This help.

Example: /usr/lib/nagios/plugins/check_traccar_device_online -i 7501043656 -t 600 -l /Path/To/Traccar/logs/tracker-server.log
OK - Device 7501043656 is online.
```
<p>
<br/>
<br/>

**Install:**

```wget -O /usr/lib/nagios/plugins/check_traccar_device_online https://raw.githubusercontent.com/unix1984/traccar_device_online/main/check_traccar_device_online && chmod  +x /usr/lib/nagios/plugins/check_traccar_device_online```
