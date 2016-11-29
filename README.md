# lightdm-webkit-theme-manjaro-dark



### Overview

A dark lightdm webkit theme with Manjaro Linux branding.

### Prerequisites
* lightdm-webkit2-greeter-manjaro

### Installation
This theme is included with `lightdm-webkit2-greeter` which is installed by default for Antergos users. Non-Antergos users should see [lightdm-webkit2-greeter](https://github.com/Antergos/lightdm-webkit2-greeter/) for installation details.

### User Icons Management

To change users icons:

* Create a resource named with the user's login in `/var/lib/AccountsService/icons/`
* Edit `/var/lib/AccountsService/users/<userLogin>` and add a property `Icon` targeting the icon resource you just created.

### Webkit2 Greeter's Theme JavaScript API:
The greeter exposes a JavaScript API to greeter themes which they must use to interact with the greeter (in order to facilitate the user login process). The [API Documentation](https://manjaro.com/wiki/development/lightdm-webkit2-greeter-theme-javascript-api/) is a W.I.P.

