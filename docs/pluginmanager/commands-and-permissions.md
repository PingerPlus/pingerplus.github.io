---
title: "Commands & Permissions"
sidebar_position: 2
---

# Commands & Permissions
Here's a quick guide on the commands and permissions you need to use to get started with Hynick:

### `/pm` (_plugin.manager.admin_)
This command opens the main GUI where you can modify plugins easily.

### `/plugin enable <pluginName>` (_plugin.manager.enable_)
Activates the specified plugin, allowing it to run on the server. Use this to turn plugins on without restarting the server.

### `/plugin disable <pluginName>` (_plugin.manager.disable_)
Deactivates the specified plugin, stopping its functionality on the server. Useful for troubleshooting or disabling unused plugins.

### `/plugin reload <pluginName>` (_plugin.manager.reload_)
Reloads the specified plugin. This applies any changes made to the plugin's settings without needing a server restart.

### `/plugin description <pluginName>` (_plugin.manager.description_)
Shows an overview of the specified plugin, including what it does and how it can be used.

### `/plugin info <pluginName>` (_plugin.manager.admin_)
Displays detailed information about the specified plugin, including its version, author, and current status (enabled or disabled).

### `/plugin commands <pluginName>` (_plugin.manager.commands_)
Lists all available commands for the specified plugin, along with their usage and permissions.

### `/plugin whitelist add <pluginName>` (_plugin.manager.whitelist_)
Adds the specified plugin to the whitelist. If the plugin is disabled, players without the `plugin.manager.bypass` permission will be kicked and won't be allowed to join the server.

### `/plugin whitelist remove <pluginName>` (_plugin.manager.whitelist_)
Removes the specified plugin from the whitelist. Players will no longer be affected if the plugin is disabled.