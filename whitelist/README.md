Whitelist Plugin
================

First working version of the whitelist plugin. Had to modify oxmin.lua to support the passing of a plugin's context. You will **need both the plugins in this gist**. 

    Commands:
    
    /whitelist [steamid]		| Adds players to the whitelist, if player is in-game you can use their in-game name.
    /blacklist [steamid]		| Remove players from the whitelist, if player is in-game you can use their in-game name.
    /whitelist_toggle			| Temporarily disables the whitelist, allowing any player to join the game.
    /whitelist_check			| Checks the current toggle status of the whitelist (i.e. enabled or disabled)

You **must have** *canwhitelist*, *canblacklist*, and *cantogglewhitelist* flags (using the oxmin giveflag command) to run these commands. The steamid supplied can be either regular (i.e. STEAM_0:1:16556317) or steamid64  (i.e. 76561197993378363). If the player is currently in-game (i.e. you disabled the whitelist via the toggle command), then you can use their in-game name and it will be automatically converted to their steamID. 


Whitelisted ids are stored in JSON format inside the server_whitelist.txt file...you can manually modify this and add the steamids, too...just make sure to keep the format correctly.

    ["first_steamid", "second_steamid", "third_steamid"]
