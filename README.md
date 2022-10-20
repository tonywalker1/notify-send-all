# notify-send-all

Uses notify-send (libnotify) to send a desktop notification to all users with a
graphical session (e.g., Gnome).

notify-send is a great tool, but it only notifies the user that runs it
(without some help). This script provides that help and allows
scripts run as root (e.g., a cron job or systemd.timer) to send
notifications to all graphical sessions.

**NOTES:**

1. This script is meant to run as root. Otherwise, sudo will ask for
   passwords for each user. Probably not something you want from a script.
2. On Debian (and probably all derivatives), you will need to install
   libnotify-bin.
3. This script does not send a message to root. This fixes a timeout 
on some distributions/desktops when attempting to send a message to root. 
Besides root should never be used as a user.

## Usage

```shell
notify-send-all "Lifeboats!" "The ship is sinking."
```

## Installation

Simply copy the file to /usr/local/bin (or similar).
