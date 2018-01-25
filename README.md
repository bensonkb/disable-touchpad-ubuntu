# disable-touchpad-ubuntu
To disable the touchpad in Ubuntu 
Put the following code in a file, such as touchpad_toggle.sh:

#!/bin/bash
STATUS=`gsettings get org.gnome.desktop.peripherals.touchpad send-events`
if [ "$STATUS" = "'enabled'" ]
then
    gsettings set org.gnome.desktop.peripherals.touchpad send-events 'disabled'
else
    gsettings set org.gnome.desktop.peripherals.touchpad send-events 'enabled'
fi

Grant the file executable permission:

chmod +x touchpad_toggle.sh
Add a keyboard shortcut to the file from Settings → Devices → Keyboard.

DISCLAIMER:- USE AT OWN RISK :-)
