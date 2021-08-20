# League of Legends Champions Statistics

## Description
This web app helps visualise and compare [LoL](https://euw.leagueoflegends.com/en-gb/) champions' base statistics using [D3](https://d3js.org/)

This project developped in the context of Isaac Pante's course "Visualisation de données" at the Université de Lausanne (UNIL). The outcome of the project can be viewed here: [https://wiola99.github.io/VD-project/] 

## Database

You can find details about the base stats of every champion in the game itself or the game's wiki [Fandom](https://leagueoflegends.fandom.com/wiki/List_of_champions/Base_statistics) but I found a downloadable csv version on [kaggle](https://www.kaggle.com/gyejr95/league-of-legendslol-champion-and-item-2020?select=riot_champion.csv) of the patch 10.6.1

Since the champion stats are constantly changing (in order to balance the game), in the future I'd like to link the app to the [Official League of Legends API](https://developer.riotgames.com/docs/lol#_getting-started) so that the data would be up to date.

## Data

Every champion in League of Legends has base stats that change as they level up (with some exceptions):

- `Attack Damage`
- `Health`
- `Mana` (some champions do not have mana)
- `Armor`
- `Magic Resistance` (often shortened to MR or here Magic Resist)
- `Health Regeneration` (HP Regen)
- `Mana Regeneration`

There are many other base stats as well (movement speed for example) but they do not increase with levels and therefore I decided not to compare them. The raw data (csv) only gives the base stat: `100 health points` for example and the stat per level `10 health points per level` so the value for each level was calculated with a function (statPerLevel()).

## Interface

**Champion selection** : You can choose two champions you want compare and search them by name.

![capture1](/img/champions.png)

**Percentage barplot** : You can quickly see which champion has higher base stat values. Simply calculated like this: `champion 1 stat % = champion 1 stat / (champion 1 stat + champion 2 stat)` and vice versa

![capture2](/img/barplot.png)

**Line graph** : Shows the selected base stat value at every level. Sometimes a champion might have a higher base stat at level 1 than another champion but a lower stat per level and the line graph helps to see if a champion will catch up or even end up having a higher base stat at some point.

![capture3](/img/lineGraph.png)

## Author

Saara Jones