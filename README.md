# MC_G_BlockCommand
Minecraft plugin to block commands for customizable groups
Minecraft version: 1.14.4
Plugin version: 0.9
<<<<<<< HEAD
Date-Modified: 21/08/19
=======

Guide:

To add/manage groups and their blocked commands refer to the config.yml file (located in your plugin folder,
please run the plugin first so it can create it's folder)

config.yml (can be copy pasted) # means it's a comment:
it's best to fill in all the attributes of a group (name and color) to prevent any errors from happening.

groups: 
  #Group 1 is the highest tier (like Owner)
  group 1: #keep it chronological (group 1, group 2, etc.) else the code won't recognize it
    name: #nameofgroup (displayed groupname)
    color: #display color (please choose a color from this list: https://hub.spigotmc.org/javadocs/spigot/org/bukkit/ChatColor.html
    members:
    - #name (name of user)
    - #name2

  #Add groups like this:
  group 2:
    name: #nameofgroup (Owner, Admin, Op, etc.)
    color: #COLOR (doesn't have to be all caps), not giving a value to color could create errors (should default to White)
    members:
      - #name
      - #name2

blocked_commands:
  #group 2 inherits from group 1, group 3 from group 2 and group 1, etc.
  #if you don't want a command to be inherited place a . before the command (like this: ./command) this way groups
  #under that group won't inherit that command
  group 1:
    - #/command1
    - #/command2

  #Add groups like this:
  group 2:
    - /gsetgroup
    - /ghelp
    - #/commandexample

broadcast-blockedcommand-public: false #decides whether or not to publicly broadcast a permission error message
                                       #("player tried to execute command but didn't have the permissions to do so")
                                       #setting it to false will only inform the player trying the command

-END of config.yml


Commands:
/ghelp            - displays the link to this file
/ggroup 					- displays the group of the player running the command
/ggroups   					- displays all groups available
/ggetgroup [player]			- displays the group of the selected player
/gsetgroup [player] [group] - removes selected user from their current group and adds them to the selected group
*caution* using /gsetgroup will most likely remove all comments in the file.
>>>>>>> 2b1a53aaa1f2f972536f410db59850353d91cdce
