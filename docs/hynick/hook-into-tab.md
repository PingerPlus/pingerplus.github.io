---
title: "How to hook into TAB?"
sidebar_position: 5
---

# How to hook into TAB?
Hooking into TAB is pretty simple. Most of the job is already done by Hynick, changing your nickname, rank and skin.

However, depending on your current configuration of TAB, your tab name and nametag name might not get updated automatically, because they simply depend on another placeholder (by default it's an Essentials placeholder) which doesn't get updated on the player.

This is the reason we have to manually change the configuration, in order to get the result we want!

**To fix this, there are 3 steps you need to follow:**
1. Install the `Player` PAPI extension on your server by doing: `/papi ecloud download Player` and `/papi reload`
2. Go into TAB `config.yml` file and enable `unlimited-nametag-mode` (you can `CTRL + F` to find it faster since the config is quite messy)
3. Go into TAB `groups.yml` file and set `customtabname` and `customtagname` to: `"%player_name%"`

You can now refresh the TAB plugin by doing `/tab reload` and you're good to go!