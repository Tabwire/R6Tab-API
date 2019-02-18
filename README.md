<p align="center">
  <h1 align="center">Official R6Tab API Documentation</h3>
</p>

## About
- Please note that We are offering this API to all of the users in the community who would to get creative with our data.

## Limitations
- There are no limitations to this API as long as it is not abused. We hold the right to refuse service to anyone who we believe is abusing this system.

## Search via platform and name
- https://r6tab.com/api/search.php?platform=XXXXX&search=YYYYY

## Search via player ID
- To find a players ID you can go to https://www.r6tab.com and search for a user. Once you are on the users page there will be a long series of letters and numbers after the .com in r6tab. These letters and numbers are the users ID.
- When you search for a player by using and ID you must use `p_id=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx` just like below
`https://r6tab.com/api/player.php?p_id=xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx`

## Call the leaderboard
- Please note that players that are banned on R6Tab will not appear on this list
- To call the leaderboard you must supply a `sortplatform` and a `sortregion`

METHOD | **sortplatform**:

- ```p_currentmmr``` will sort the players by MMR for all regions<br>
- ```p_NA_currentmmr``` will sort the players by MMR for the American region<br>
- ```p_EU_currentmmr``` will sort the players by MMR for the European region<br>
- ```p_AS_currentmmr``` will sort the players by MMR for the Asian region<br>
- ```p_skillrating``` will sort the players by Tabrank ELO<br>
- ```p_headshotacc``` will sort the players by headshot accuracy percentage<br>

METHOD | **sortregion**:

- `uplay` will only display PC players<br>
- `psn` will only display Playstation players<br>
- `xbl` will only display Xbox players<br>


## Affiliation
- The R6Tab API is in no way shape or form affiliated with Ubisoft and its partners. Any "Rainbow Six: Siege" name, logos and/or images are registered trademarks of Ubisoft.
