Minecraft Denizen Plugin Scripts
===========

Open source Denizen scripts for Minecraft Servers running Craft Bukkit 1.7.5 + with the Citizens 2 and Denizen plugins.

```YAML
# This script will prevent anyone who is not Aayrl
# from placing or breaking blocks in the Plane of Ender.

"AntiEnderGrief":
  type: world
  events:
    on player places block:
      - if <player.location.world.name> == "world_the_end" {
        - if <player.name> != "Aayrl" && <player.name> != "lenois" {
          - narrate "<&9>Magical forces prevent you from building here."
          - determine cancelled
          }
        }
```
