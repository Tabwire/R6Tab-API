<p align="center">
  <h1 align="center">Official R6Tab API Documentation</h3>
</p>

## About
- Please note that We are offering this API to all of the users in the community who would to get creative with our data.

## Limitations
- There are no limitations to this API as long as it is not abused. We hold the right to refuse service to anyone who we believe is abusing this system.

<hr>

## Search by name

Request URL {GET} https://r6tab.com/api/search.php

METHOD | **name**:

- <i>**playername**</i> urlencode the playername<br>


METHOD | **platform**:

- <i>**uplay**</i> will only display PC players<br>
- <i>**psn**</i> will only display Playstation players<br>
- <i>**xbl**</i> will only display Xbox players<br>

Response data:

- <i>**p_id**</i> is the Identifier assigned by ubisoft to the player<br>
- <i>**p_name**</i> is the current name of the player<br>
- <i>**p_level**</i> is the current level of the player<br>
- <i>**p_level**</i> is the current level of the player<br>
- <i>**p_level**</i> is the current level of the player<br>
- <i>**p_level**</i> is the current level of the player<br>
- <i>**p_level**</i> is the current level of the player<br>
- <i>**kd**</i> is the average Kill to Death ratio for the player<br>

Note that <i>**p_user**</i> does not always match to <i>**p_id**</i> {p_user} can be used to grab the player avatar: `https://ubisoft-avatars.akamaized.net/p_user/default_146_146.png`


Example: https://r6tab.com/api/search.php?platform=uplay&search=Baiier

Example response:
```
{
  "results": [
    {
      "p_id": "9bd44bde-9c48-48ae-9c2b-4e11e4b16083",
      "p_name": "BaIIer",
      "p_level": "341",
      "p_platform": "uplay",
      "p_user": "9bd44bde-9c48-48ae-9c2b-4e11e4b16083",
      "p_currentmmr": "3979",
      "p_currentrank": "18",
      "kd": "128"
    },
    {
      "p_id": "83518584-ac1e-4a56-838c-be78f02a523b",
      "p_name": "BaIIer101",
      "p_level": "24",
      "p_platform": "uplay",
      "p_user": "83518584-ac1e-4a56-838c-be78f02a523b",
      "p_currentmmr": "0",
      "p_currentrank": "0",
      "kd": "0"
    }
  ],
  "totalresults": 2
}
```
<hr>

## Search via player ID
- To find a players ID you can go to https://www.r6tab.com and search for a user. Once you are on the users page there will be a long series of letters and numbers after the .com in r6tab. These letters and numbers are the users ID.
- When you search for a player by using and ID you must use `p_id=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx` just like below
`https://r6tab.com/api/player.php?p_id=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx`

<hr>

## Call the leaderboard
- Please note that players that are banned on R6Tab will not appear on this list and that **the leaderboard is refreshed every hour**
- To call the leaderboard you must supply a <i>**sortplatform**</i> and a <i>**sortregion**</i> to the request

METHOD | **sortplatform**:

- <i>**p_currentmmr**</i> will sort the players by MMR for all regions<br>
- <i>**p_NA_currentmmr**</i> will sort the players by MMR for the American region<br>
- <i>**p_EU_currentmmr**</i> will sort the players by MMR for the European region<br>
- <i>**p_AS_currentmmr**</i> will sort the players by MMR for the Asian region<br>
- <i>**p_skillrating**</i> will sort the players by Tabrank ELO<br>
- <i>**p_headshotacc**</i> will sort the players by headshot accuracy percentage<br>

METHOD | **sortregion**:

- <i>**uplay**</i> will only display PC players<br>
- <i>**psn**</i> will only display Playstation players<br>
- <i>**xbl**</i> will only display Xbox players<br>

## Leaderboard call example
- An example of a leaderboard call would be:

<i>**https://r6tab.com/api/leaderboards.php?sortplatform=uplay&sortregion=p_NA_currentmmr**</i>

This will result in a few thing

<hr>

## Affiliation
- The R6Tab API is in no way shape or form affiliated with Ubisoft and its partners. Any "Rainbow Six: Siege" name, logos and/or images are registered trademarks of Ubisoft.
