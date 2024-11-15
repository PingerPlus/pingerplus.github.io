---
title: "Installation & Configuration"
sidebar_position: 3
---

# Installation & Configuration
# Installation
1. Download the `PluginManagerPlus` plugin jar file from one of the sites: **Spigot, BuiltByBit, Polymart.**
1. Place the downloaded jar files into the "plugins" folder in your Minecraft server directory.
1. Restart your Minecraft server to load the PluginManagerPlus plugin.

# Configuration
* [`messages.yml`](#messagesyml) - Where all messages sent to the user are stored (which you can edit)

Most of the time if you need a cross-server support, you can just turn on the database and setup the credentials and then restart the server.

### messages.yml
This file contains all messages sent to the player by message. <br/>
You can edit each of these messages, where you should only not remove `%s` because that is a parameter that will later on be set to a value depending on the message. For example, in the `'&c%s has been disabled, which is a whitelisted plugin.'` message the `%s` will get set to whatever the plugin name is that is being disabled.

You can see the current contents of the messages.yml file below:
```yml title="messages.yml"
request:
  failed: "&cCould not complete the requested action. \nResponse: &e%s"
  kick-reason: "&c%s has been disabled, which is a whitelisted plugin."
  prevent-join: "&cOne or more of whitelisted plugins has been disabled"

plugins:
  refreshed: "&aSuccessfully refreshed the plugins folder. "
  enable: "&e&l%s &ahas been enabled successfully"
  disable: "&e&l%s &ahas been disabled successfully"
  reloaded: "&e&l%s &ahas been reloaded successfully. \nResponse: &e%s"
  description: "&b&lDescription: "
  disable-associated: "&aSuccessfully disabled %s out of %s plugins associated \nwith this plugin."
  whitelist-add: "&e%s has been successfully added to the whitelist"
  whitelist-remove: "&c%s has been successfully removed from the whitelist"

common:
  undefined: "&e - Not defined"
  invalid-args: "&cCould not recognize the argument pattern. "

commands:
  fail-register: "&cFailed to register the %s command"
  fail-unregister: "&cFailed to unregister the %s command"
  register: "&aSuccessfully registered the %s command"
  unregister: "&aSuccessfully unregistered the %s command"

user:
  opening: "&aOpening the requested data inventory."
```