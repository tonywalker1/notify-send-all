# notify-send-all
Uses notify-send to notify all GUI users.

notify-send is a great tool, but it only notifies the user that runs the
script (without some help). This script provides that help and allows 
scripts run as root (e.g., a cron job or systemd.timer).

**NOTE:** This script is meant to run as root. Otherwise, sudo will ask for 
passwords for each user. Probably not something you want from a script.

## Usage

```shell
notify-send-all "Lifeboats!" "The ship is sinking."
```
