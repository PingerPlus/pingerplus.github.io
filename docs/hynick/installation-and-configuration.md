---
title: "Installation & Configuration"
sidebar_position: 3
---

# Installation & Configuration
# Installation
1. Download the Hynick and DisguiseAPI plugin jar files from one of the sites: **Spigot, BuiltByBit, Polymart.**
1. Place the downloaded jar files into the "plugins" folder in your Minecraft server directory.
1. Restart your Minecraft server to load the Hynick plugin.

# Configuration
After **Hynick** has been installed on your system, a folder named Hynick will be generated inside of your "plugins" folder with the following files:
* [`config.yml`](#configyml) - For general settings of the plugins
* [`messages.yml`](#messagesyml) - Where all messages sent to the user are stored (which you can edit)
* [`pages.json`](#pagesjson) - Generated JSON file containing the contents of all pages.
* [`ranks.yml`](#ranksyml) - For setting up nick ranks

You can read about each of these files individually down below to find how to edit them correctly.
When you finish editing these files you can do `/hynick reload` to reload those files without having to restart the server

### config.yml
This file is fully documented, you can open it in an editor to simply see what changes you should make. <br/>
Most of the time if you need a cross-server support, you can just turn on the database and setup the credentials and then restart the server.

### messages.yml
This file contains all messages sent to the player by message (not in books). <br/>
You can edit each of these messages, where you should only not remove `%s` because that is a parameter that will later on be set to a value depending on the message. For example, in the `'&aSet your nick rank to %s&a!'` message the `%s` will get set to whatever the rank name is that the player chooses.

You can see the current contents of the messages.yml file below:
```yml title="messages.yml"
rank:
  set: '&aSet your nick rank to %s&a!'
nick:
  finished: '&aYou have finished setting up your nickname!'
  generating: '&eGenerating a unique random name. Please wait...'
  reuse: '&aYour name has been set to ''%s'''
  reset: '&aYour nick has been reset!'
  not-have: '&cYou are not nicked currently!'
skin:
  normal: '&aYour skin has been set to yourself'
  alex: '&aYou will now show up as an Alex.'
  random: '&aYour skin was selected randomly!'
  reuse: '&aYour skin has been set to the previous one!'
```

### pages.json
This file is a JSON generated file containing default pages for books that are opened to the player when the /nick command is executed.
When editing this file, you **may only change the text fields of the json (`wherever is says "text": "..."**`). <br/>
Editing anything else might cause issues with the plugin, since the pages are overridden from this file.
If you for some reason do get an error after you've edited this file, you can revert to the old file by restarting your server and deleting the file.

Down below is an example of the first page generated inside the `pages.json` file:
```json title="pages.json"
[
  {
    "1": {
      "text": "Nicknames allow you to play with a different username to not get recognized.\n"
    }
  },
  {
    "2": {
      "text": "\nAll rules still apply. You can still be reported and all name history is stored.\n"
    }
  },
  {
    "confirm": {
      "text": "\n➤ §nI understand, set §nup my nickname",
      "clickable": true,
      "hover": {
        "value": [
          {
            "text": "Click here to proceed"
          }
        ]
      }
    }
  }
]
```

### ranks.yml
You can use this page to edit any rank or add your own custom ranks that will be assigned to a player. <br/>

Each rank has the following properties:
1. `permission` - The permission needed to be able to use this rank in the gui
1. `name` - This is the name that will be displayed in the gui with the provided formatting (custom color...)
1. `prefix` - This is the prefix that will be used in the TAB and Vault plugins automatically

All players who can access the `/nick` **must have permission for at least 1 rank when executing it.**

By default (from the Hypixel model), there are 5 ranks: **default, vip, vip+, mvp, mvp+**:

```yml title="ranks.yml"
default:
  permission: ""
  name: "&7DEFAULT"
  prefix: "&7 "
vip:
  permission: "permission.hynick.vip"
  name: "&aVIP"
  prefix: "&a[VIP] "
vip+:
  permission: "permission.hynick.vip+"
  name: "&aVIP&6+"
  prefix: "&a[VIP&6+&a] "
mvp:
  permission: "permission.hynick.mvp"
  name: "&bMVP"
  prefix: "&b[MVP] "
mvp+:
  permission: "permission.hynick.mvp+"
  name: "&bMVP&c+"
  prefix: "&b[MVP&c+&b] "
```




