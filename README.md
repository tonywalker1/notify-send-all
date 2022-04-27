# notify-send-all
Uses notify-send to notify all GUI users.

notify-send is a great tool, but it only notifies the user that runs the
script (without some help). This script provides that help and allows 
scripts run as root (e.g., a cron job or systemd.timer).

**NOTE 1:** This script is meant to run as root. Otherwise, sudo will ask for 
passwords for each user. Probably not something you want from a script.

**NOTE 2:** This script does not send a message to root. This fixes a timeout 
on some distributions/desktops when attempting to send a message to root. 
Besides root should never be used as a user.

## Usage

```shell
notify-send-all "Lifeboats!" "The ship is sinking."
```

## Installation

Simply copy the file to /usr/local/bin (or similar).
