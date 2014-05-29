Minecraft Denizen Plugin Scripts
===========

Open Source Denizen scripts for Minecraft Servers running Craft Bukkit 1.7.5+ 
Requires the Citizens2, Sentry, and Denizen plugins.

## Requirements

### Server Requirements 

In order to run these scripts on your server, you will need to be running [Craft Bukkit 1.7.5](https://dl.bukkit.org/downloads/craftbukkit/) or greater. Our server currently uses [Craft Bukkit 1.7.5-R0.1](https://dl.bukkit.org/downloads/craftbukkit/view/02566_1.7.5-R0.1/), and we will continue to support this version of CB until a build compatible with Minecraft 1.8 is released (pending).

### Plugin Requirements

You are also **required to have the following plugins** installed on your Craft Bukkit server in order for these scripts to work properly:
- [Denizen](http://dev.bukkit.org/bukkit-plugins/denizen/) for handling all of the scripts submitted to this repository.
- [Citizens2](http://dev.bukkit.org/bukkit-plugins/citizens/) for handling the scripts that require NPCs.
- [Sentry](http://dev.bukkit.org/bukkit-plugins/sentry-citizens2/) for handling scripts that require special NPCs such as boss mobs and guards.

The following plugins are *recommended* (and may be used by some of these scripts), but are not required:
- [Multiverse2 & Multiverse2 Portals](http://dev.bukkit.org/bukkit-plugins/multiverse-core/) for usage with multi-world scripts and scripts that use multiverse commands.
- [Better Backpacks](http://dev.bukkit.org/bukkit-plugins/better-backpacks/) for usage with Backpack Vendor script and Backpack scripts.
- [HealthBar](http://dev.bukkit.org/bukkit-plugins/health-bar/) compatible with Sentry and Citizens plugin!

## Usage

The scripts found on this repository are actively used on our own private Minecraft Server. There are plans to open this server up to the public in the future, but for the moment is only available to our local network.

### Automated Minecraft Script Updates

If you wish to use some (or all) of these scripts on your own Minecraft server, you can force update these scripts fairly easily by creating a batch file with the following contents:
```Batchfile
cd C:\SERVER_ROOT_DIRECTORY_HERE\plugins\Denizen\scripts\
git pull
```
You can automate this process to have it run on your Minecraft Server through a scheduled task and thus automatically update the script files. You can even build a fairly simple Denizen script to auto-reload scripts periodically to account for the updated script files like so:
```YAML
# This script will automatically reload Denizen scripts 
# roughly every 15 minutes.
"ReloadDenizenScripts":
  type: world
  events:
    on 0:00 in w@world:
      - announce "<green><&lb><&d>SERVER<green><&rb> Reloading Denizen Scripts..."
      - execute as_server "denizen reload scripts"
      - announce "<green><&lb><&d>SERVER<green><&rb> Done!"
```

### Scripts in Action

You may be able to see some of our scripts in action by viewing the [Gallery](https://github.com/Aayrl/mc_denizens/tree/master/Photos) section of the repository.

### File Naming Conventions

The files in our repository are named appropriately and should provide ample information about the contents of each script. The first word of each filename determines what class of script it contains, and the preceeding works describe the class specifications. Currently, we have the following categories:
- **BOSS** : These are 'Boss' (strong) NPCs with valuable loot associated with them.
- **CHAT** : Any scripts that create or modify existing chat commands, such as emotes and chat channels.
- **CMD** : Custom scripted commands that players may use on our servers as they would with normal Minecraft commands. Example usage: /commands
- **FACTION** : Custom scripted factions associated with certain NPCs, as well as initializers for faction support through Denizen flags.
- **ITEM** : Denizen scripted custom items that players can obtain in-game. Some items have custom effects that may also be present in their respective item script files.
- **MOB** : These are hostile NPCs that are more challenging than traditional Minecraft hostile mobs.
- **NPC** : Various NPC script files, such as guards, blacksmiths, or even questgivers. 
- **QUEST** : Quest script files in the form of NPC assignments that you may assign for any Citizens NPC.
- **SCRIPT** : Miscellaneous script files that simply process information and produce results. This can range from server mechanic enhancements to custom server scoreboard handling.
- **SPELL** : Custom spell scripts that allow players to craft and use powerful spells. Think of these as an alternative to Potions. Spells use a player's hunger bar as the 'mana' bar for those familiar with MMO terminology.
- **UNUSED** : Scripts that were designed as test scripts or are currently unused, but still kept in the repository for reference in future scripts.

## Contributors

- [Aayrl](https://github.com/Aayrl) : Primary Developer
- [cartmensfoe](https://github.com/cartmensfoe) : Assistant Questline and Command Script Development
- [Lenois](https://github.com/Lenois) : Assistant Script Developer

## Licenses and Script Notices

For information regarding the licenses for the Denizen plugin and other respective plugins mentioned, please visit the associated plugin repositories.

As a further notice, all scripts that are provided in this repository are fashioned for usage on Minecraft Servers and do not endorse any third parties. These scripts are made publicly available for free and will never be offered as a result of a premium.

Any ficticious content that makes references to other copyrighted material (such as item names or NPC names that may be familiar to ones seen in other video games) are purely aesthetic and are **not** associated with their respective counterparts in any way. If you feel some of the content in these scripts infringes their counterparts, we ask that you please notify us so that we may make the aesthetic changes to meet with your wishes. It's strongly emphasized that these scripts are our work, and any names for the scripts or contents within the scripts are coincidental and credit will be given to those that demonstrate they deserve it.