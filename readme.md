

### Python Modules Used:
paho.mqtt.client as mqtt
mfrc522
numpy as np
pandas as pd
time
RPi.GPIO as GPIO
os
datetime
threading

### sshfs commands:

sshfs:

    sshfs user@hostname.local: directory

unmount:

    sudo umount directory

or:

    sudo diskutil umount force directory

### mqtt server:

eclipse-mqtt server startup command:

    docker run -i -p 1883:1883 -p 9001:9001 -v /home/pi/docker/mosquitto.conf:/mosquitto/config/mosquitto.conf -v /mosquitto/data -v /mosquitto/log eclipse-mosquitto

### raspi system log check:

syslog:

    cat /var/log/syslog | grep foo

Running in `/etc/rc.local`:
 - docker eclipse-mqtt server
 - python scripts

### Misc:

    ps aux | grep python

#### Updates:
- `12-1-20`: Adding detection of unlock from a keypad (GPIO High->Low trigger)