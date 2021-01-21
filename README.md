LibRealmInfo
===============

Library to provide information about realms.

* [Download on CurseForge](https://wow.curseforge.com/projects/librealminfo)
* [Download on WoWInterface](https://www.wowinterface.com/downloads/info22987-LibRealmInfo.html)
* [Source Code on GitHub](https://github.com/phanx-wow/LibRealmInfo)
* [Issue Tracker on GitHub](https://github.com/phanx-wow/LibRealmInfo/issues)


Documentation
----------------

* [API functions](https://github.com/phanx-wow/LibRealmInfo/wiki/API)
* [Adding LibRealmInfo to your addon](https://github.com/Phanx/LibRealmInfo/wiki/Embedding)


Caveats
----------

If you only need to know the names of realms connected to the player's current realm, you should just use [GetAutoCompleteRealms](http://wowpedia.org/API_GetAutoCompleteRealms) instead of this library.

If you only need to know which region (US, Europe, etc.) the player is currently in, you can try [GetCurrentRegion](http://wowpedia.org/API_GetCurrentRegion), but you should be aware that this function may return incorrect values for players whose game clients have connected to multiple regions.

### Realm IDs in player GUIDs are not reliable

The realm IDs encoded in the GUIDs of player characters on connected realms identify the server currently hosting the connected realm group, which may not be the realm that character actually belongs to. Pass the GUID to [GetPlayerInfoByGUID](http://wowpedia.org/API_GetPlayerInfoByGUID) to get the character's real realm name, or use the `GetRealmInfoByGUID` or `GetRealmInfoByUnit` methods provided by LibRealmInfo.

### Note on US Server Timezones
Blizzard has a tendancy to change the timezones of Mainland US servers during realm connections, All realms in a cluser use the timezone assigned to the "Host server". Up to date timezone information can be sourced here: https://worldofwarcraft.com/en-us/game/status/us

### Note on Chinese servers
English translations of are taken from official Blizzard sources where possible (Hall of Fame, PTR char transfer etc), in some cases, particilarly with Classic servers, I have not been able to extract all the names and have manually translated some of them, this could result in some minor indescreptencies. Blizzards Server list for Chinese servers is only availible in Chinese, and thus its impossible to extract english server names from it. I make no guarientee that all the translations are 100% correct with Blizzards naming of the server but will do my best to update any errors found.
