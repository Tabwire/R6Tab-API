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

- <i>**aid**</i> is the Identifier assigned by ApexTab to the player<br>
- <i>**name**</i> is the current name of the player<br>
- <i>**platform**</i> is the platform of the player<br>
- <i>**level**</i> is the current level of the player<br>
- <i>**kills**</i> is the current total kills of the player<br>
- <i>**avatar**</i> is the current avatar URL of the player<br>
- <i>**legend**</i> is the current selected legend of the player<br>

Example: https://apextab.com/api/search.php?platform=pc&search=tinybaiier

Example response:
```
{
  "results": [
    {
      "aid": "f5337d769b7b29628f59d8c84ea45d9d",
      "name": "TinyBaIIer",
      "platform": "pc",
      "avatar": "https://apextab.com/cache/fc4c4cba183c2f81a94730be057cf07d.png",
      "legend": "Pathfinder",
      "level": "19",
      "kills": "44"
    }
  ],
  "totalresults": 1
}
```
<hr>

## Affiliation
- The ApexTab API is in no way shape or form affiliated with Electronic Arts and its partners. Any "Apex Legend" name, logos and/or images are registered trademarks of EA Games and/or Respawn.
