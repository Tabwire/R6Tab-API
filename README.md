<p align="center">
  <h1 align="center">Official R6Tab API Documentation</h3>
</p>

<hr>

## About
- Please note that We are offering this API to all of the users in the community who would to get creative with our data.

## Limitations
- There are no limitations to this API as long as it is not abused. We hold the right to refuse service to anyone who we believe is abusing this system.

<hr>

## Search by name

Request URL {GET} https://r6tab.com/api/search.php

METHOD | **platform**:

- <i>**uplay**</i> will only display PC players<br>
- <i>**psn**</i> will only display Playstation players<br>
- <i>**xbl**</i> will only display Xbox players<br>

METHOD | **search**:

- <i>**playername**</i> URL encode the playername<br>

Response data:

- <i>**p_id**</i> is the Identifier assigned by Ubisoft to the player<br>
- <i>**p_name**</i> is the current name of the player<br>
- <i>**p_level**</i> is the current level of the player<br>
- <i>**p_platform**</i> is player's platform (uplay, psn, xbl)<br>
- <i>**p_user**</i> is the Identifier assigned by Ubisoft to the player<br>
- <i>**p_currentmmr**</i> is the current MMR of the player<br>
- <i>**p_currentrank**</i> is the current MMR based Rank of the player (see: <u>[Ranks.md](https://github.com/Tabwire/R6Tab-API/blob/master/Ranks.md)</u>)<br>
- <i>**verified**</i> is the custom Identifier assigned by TabWire to check if the player is verified<br>
- <i>**kd**</i> is the Kill to Death ratio for the player<br>

Note that <i>**p_user**</i> does not always match to <i>**p_id**</i>

<i>**p_user**</i> can be used to grab the player avatar: 
`https://ubisoft-avatars.akamaized.net/p_user/default_146_146.png`

Example: https://r6tab.com/api/search.php?platform=uplay&search=Baiier

Example response:
```
{
  "results": [
    {
      "p_id": "9bd44bde-9c48-48ae-9c2b-4e11e4b16083",
      "p_name": "BaIIer",
      "p_level": "366",
      "p_platform": "uplay",
      "p_user": "9bd44bde-9c48-48ae-9c2b-4e11e4b16083",
      "p_currentmmr": "3979",
      "p_currentrank": "18",
      "verified":1,
      "kd": "122"
    },
    {
      "p_id": "54dd1deb-0a93-4be1-b36d-3ff53f43f9fb",
      "p_name": "BaIIer..",
      "p_level": "147",
      "p_platform": "uplay",
      "p_user": "54dd1deb-0a93-4be1-b36d-3ff53f43f9fb",
      "p_currentmmr": "0",
      "p_currentrank": "0",
      "verified":0,
      "kd": "112"
    }
  ],
  "totalresults": 2
}
```
<hr>

## Get player's data by ID

Request URL {GET} https://r6tab.com/api/player.php

METHOD | **p_id**:

- <i>**playerid**</i> is the ID that Ubisoft assigns to every player.<br>

An example of a player ID is: <i>**9bd44bde-9c48-48ae-9c2b-4e11e4b16083**</i>

Example: https://r6tab.com/api/player.php?p_id=9bd44bde-9c48-48ae-9c2b-4e11e4b16083

Example response: <u>[playerdatabyid.json](https://github.com/Tabwire/R6Tab-API/blob/master/responses/playerdatabyid.json)</u>

Operators IDs: <u>[Operators.md](https://github.com/Tabwire/R6Tab-API/blob/master/Operators.md)</u>

Data IDs: <u>[Data.md](https://github.com/Tabwire/R6Tab-API/blob/master/Data.md)</u>

<hr>

## Call the leaderboard

Request URL {GET} https://r6tab.com/api/leaderboard.php<br>
- Please note that players that are banned on R6Tab will not appear on this list and that **the leaderboards are refreshed every hour**<br>
- To call the leaderboard you must supply a <i>**sortplatform**</i> and a <i>**sortregion**</i> to the request<br>

METHOD | **sortplatform**:

- <i>**uplay**</i> will only display PC players<br>
- <i>**psn**</i> will only display Playstation players<br>
- <i>**xbl**</i> will only display Xbox players<br>

METHOD | **sortregion**:

- <i>**p_currentmmr**</i> will sort the players by MMR for all regions<br>
- <i>**p_NA_currentmmr**</i> will sort the players by MMR for the American region<br>
- <i>**p_EU_currentmmr**</i> will sort the players by MMR for the European region<br>
- <i>**p_AS_currentmmr**</i> will sort the players by MMR for the Asian region<br>
- <i>**p_skillrating**</i> will sort the players by Tabrank ELO<br>
- <i>**p_headshotacc**</i> will sort the players by headshot accuracy percentage<br>

Example: https://r6tab.com/api/leaderboards.php?sortplatform=psn&sortregion=p_currentmmr

Example response: <u>[leaderboardresponse.json](https://github.com/Tabwire/R6Tab-API/blob/master/responses/leaderboardresponse.json)</u>

<hr>

## Affiliation
- The R6Tab API is in no way shape or form affiliated with Ubisoft and its partners. Any "Rainbow Six: Siege" name, logos and/or images are registered trademarks of Ubisoft.
