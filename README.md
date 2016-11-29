# lightdm-webkit-theme-manjaro-dark



### Overview

A dark lightdm webkit theme with Manjaro Linux branding.

### Prerequisites
* lightdm-webkit2-greeter-manjaro

### Installation
WARNING: Installing lightdm themes could break your display manager and leave you with a TTY terminal. If you are not confident that you could recover from this situation, please don't try to install this theme manually.

    You need the lightdm-webkit2-greeter-manjaro package from the repositories, so search for it in your preferred package manager or run:
    sudo pacman -S lightdm-webkit2-greeter-manjaro
    And obviously you will need to download and extract the theme from github (See the bottom of this post).

    Rename the extracted theme folder to "manjaro-dark" - this is important.
    Copy the extracted theme folder to /usr/share/lightdm-webkit/themes.
    sudo cp -R /where/you/extracted/the/files/manjaro-dark /usr/share/lightdm-webkit/themes

    Make backups of your /etc/lightdm/lightdm.conf and /etc/lightdm/lightdm-webkit2-greeter.conf files.
    sudo cp /etc/lightdm/lightdm.conf /etc/lightdm/lightdm.conf.old
    sudo cp /etc/lightdm/lightdm-webkit2-greeter.conf /etc/lightdm/lightdm-webkit2-greeter.conf.old

    Edit your /etc/lightdm/lightdm.conf file to use the lightdm-webkit-greeter (if you already use a webkit greeter skip this step).
    sudo nano /etc/lightdm/lightdm.conf
    You want to uncomment and change the "greeter-session" line to equal lightdm-webkit2-greeter. However I noticed in my file there was more than one line with "greeter-session", so do the one which is near the desktop environment you use.

    Edit your /etc/lightdm/lightdm-webkit2-greeter.conf file to use the manjaro-dark theme.
    sudo nano /etc/lightdm/lightdm-webkit2-greeter.conf
    You just need to change the "webkit-theme" line to equal "manjaro-dark".

    Reboot, and hopefully the new theme will appear.


### User Icons Management

To change users icons:

* Create a resource named with the user's login in `/var/lib/AccountsService/icons/`
* Edit `/var/lib/AccountsService/users/<userLogin>` and add a property `Icon` targeting the icon resource you just created.

### Webkit2 Greeter's Theme JavaScript API:
The greeter exposes a JavaScript API to greeter themes which they must use to interact with the greeter (in order to facilitate the user login process). The [API Documentation](https://manjaro.com/wiki/development/lightdm-webkit2-greeter-theme-javascript-api/) is a W.I.P.

