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

Request URL {GET} https://r6.apitab.com/search/{platform}/{name}

PATH | **platform**:

- <i>**uplay**</i> will only display PC players<br>
- <i>**psn**</i> will only display Playstation players<br>
- <i>**xbl**</i> will only display Xbox players<br>

PATH | **name**:

- <i>**playername**</i> urlencode the playername<br>

PARAMETER | **u**:

- <i>**unix**</i> provide the unix timestamp to avoid caching

#### Response Data:

- <i>**status**</i> is the code returned if the request was successful<br>
- <i>**foundmatch**</i> is a `boolean` depicting if any matches were found<br>
- <i>**requested**</i> is the requested ubisoft id sent to the API<br>
- <i>**players**</i> is a `JSON` object containing ubisoft player IDs with their own JSON Object<br>

#### Players Object:
<i> **profile**</i>
- <i>**p_id**</i> is the identifier assigned by ubisoft to the player. (Can be used as `p_user`)<br>
- <i>**p_user**</i> is the identifier assigned by ubisoft to the player. (Can be used as `p_id`)<br>
- <i>**p_name**</i> is the current name of the player<br>
- <i>**p_platform**</i> is the platform of the player<br>
- <i>**verified**</i> is a `boolean` depicting if the player is verified<br>

<i>**refresh**</i><br>
- <i>**x**</i> is the last time stats updated<br>
- <i>**s**</i> is last time profile was edited (Premium members)<br>

<i> **stats**</i><br>

- <i>**level**</i> is the level of the player.<br>

<i> **ranked**</i>: <u>[Click Here](https://github.com/Tabwire/R6Tab-API/blob/master/responses/playersdatabyname.json#L21)</u><br>

Example: https://r6.apitab.com/search/uplay/BaIIer?u=1585761495

Example response: <u>[Click Here](https://github.com/Tabwire/R6Tab-API/blob/master/responses/playersdatabyname.json)</u>

<hr>

## Get player data by ID

Request URL {GET} https://r6.apitab.com/player/{p_id}

PATH | **p_id**:

- <i>**playerid**</i> is the ID that Ubisoft assigns to every player.<br>

PARAMETER | **u**:

- <i>**unix**</i> provide the unix timestamp to avoid caching

An example of a player ID is: <i>**9bd44bde-9c48-48ae-9c2b-4e11e4b16083**</i>

Example: https://r6.apitab.com/player/9bd44bde-9c48-48ae-9c2b-4e11e4b16083?u=1585761495

Example response: <u>[Click Here](https://github.com/Tabwire/R6Tab-API/blob/master/responses/playerdatabyid.json)</u>

Operators IDs: <u>[Click Here](https://github.com/Tabwire/R6Tab-API/blob/master/Operators.md)</u>

Data IDs: <u>[Click Here](https://github.com/Tabwire/R6Tab-API/blob/master/Data.md)</u>

<hr>

## Update player data by ID

Request URL {GET} https://r6.apitab.com/update/{p_id}

PATH | **p_id**:
- <i>**playerid**</i> is the ID that Ubisoft assigns to every player.<br>

Please note, 1800 seconds need to pass for the profile to refresh. If an update request is sent sooner, the request will redirect.

## Call the leaderboard

Request URL {GET} https://r6.apitab.com/leaderboards/{platform}/{region}<br>
- Please note that players that are banned on R6Tab will not appear on this list and that **the leaderboards are refreshed every hour**<br>

PATH | **platform**:

- <i>**uplay**</i> will only display PC players<br>
- <i>**psn**</i> will only display Playstation players<br>
- <i>**xbl**</i> will only display Xbox players<br>

PATH | **region**:

- <i>**america**</i> will return top 100 Americanan players<br>
- <i>**europe**</i> will return top 100 European players<br>
- <i>**asia**</i> will return top 100 Asian players<br>
- <i>**all**</i> will return top 100 players in the world<br>

PARAMETER | **u**:

- <i>**unix**</i> provide the unix timestamp to avoid caching

Example: https://r6.apitab.com/leaderboards/uplay/america?u=1585761495

Example response: <u>[Click Here](https://github.com/Tabwire/R6Tab-API/blob/master/responses/leaderboardresponse.json)</u>

<hr>

## Affiliation
- The R6Tab API is in no way shape or form affiliated with Ubisoft and its partners. Any "Rainbow Six: Siege" name, logos and/or images are registered trademarks of Ubisoft.
