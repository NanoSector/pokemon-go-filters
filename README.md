# Pokemon Go Filters

A list of Pokémon Go filters that I commonly use. This list has been inspired by many sources, offline and online.
It is highly opinionated and might not align with how you play the game.

## Useful links

- [LeekDuck](https://leekduck.com), a well-known source for actual Pokémon Go resources
- [SearchPhrases](https://leidwesen.github.io/SearchPhrases/), an awesome overview of search strings by [leidwesen](https://github.com/leidwesen)
- [Pokémon GO Hub DB](https://db.pokemongohub.net/), information about all the Pokémon in the game
- [MonGoSearch](https://github.com/Lebeg134/MonGoSearch), a tool to create search strings with complex statements
  - [pkgosearch](https://pkgosearch.com/), a newer alternative by aalexandree-g ([GitHub](https://github.com/aalexandree-g/pkgosearch))

## Objectives

The filters and tags are centered around the following objectives:

- Complete the Pokédex;
    - Collect at least one of every Pokémon,
    - Collect one of every variant,
    - Ideally keep a living dex (however, this has a higher management overhead than I would like).
- Keep special Pokémon;
    - Hundo (100% IV),
    - Nundo (0% IV),
    - Shinies,
    - XXL (for showcases),
    - Event (including backgrounds),
    - Level 1 (10 CP),
    - "Rare"/Opportunistic, e.g. Rotom.

## Tags

I use the following tags in the following order for quick sorting. The order is pretty much determined by how often I have to use a tag but is fluid.

- The favourite tag contains buddies, to-be-buddies and other Pokémon based on personal preference.
- Any mons kept solely for trading are placed in the built-in Remote Trade tag and do not have any other tags applied. This turns my Remote Trade tag into sort of a public auction.

### 1. Objective tags

These tags match the objectives listed above. They are colored **orange**.

| Tag          | Description                                                                                                                       | Search String                                                                                    |
|:-------------|:----------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| **Shiny**    | Pokémon that are shiny.                                                                                                           | `shiny`                                                                                          |
| **Biggest**  | Pokémon that are XXL (for showcases).                                                                                             | `xxl`                                                                                            |
| **Level 1**  | Pokémon with 10 CP.                                                                                                               | `cp10`                                                                                           |
| **Hundo**    | Pokémon with 100% IV.                                                                                                             | `4*`                                                                                             |
| **Nundo**    | Pokémon with 0% IV (or close to, which I call "bijnundo", a wordplay on the Dutch word "bijna")                                   | `0attack*0defense&0hp`                                                                           |
| **Event/BG** | Pokémon which have a costume, any form of background or were only available during specific events (e.g. Spinda forms).           | `costume,background`                                                                             |
| **Rare**     | Extremely hard to get by (e.g. Rotom, antique form Sinistea). There is overlap with the Event tag but this is more of a showcase. | `151,251,385,479,480,481,482,490,492,494,647,648,719,721,789,790,791,792,802,803,890,893,999`    |

### 2. Statuses

These tags indicate Pokémon with a specific status. They are colored **red**.

| Tag                 | Description                                                                        | Search String                                                                                                                             |
|:--------------------|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| **Mega**            | Pokémon with mega evolution status.                                                | `mega1-`                                                                                                                                  |
| **AdventureEffect** | Pokémon with an adventure effect move.                                             | `adventureeffect`                                                                                                                         |
| **Level 50**        | Any mons maxed out in level.                                                       |                                                                                                                                           |
| **DoNotPurify**     | Shadow mons that rank high in raid battles according to Pokémon GO Hub tier lists. | `68,94,99,123,130,143,145,146,149,150,243,244,248,254,257,260,282,310,319,373,376,382,383,409,461,462,464,466,473,475,530,609,635&shadow` |

### 3. Actions

These tags indicate mons that require attention or an action at some point. They are colored **green**.

| Tag               | Description                                                                                                                                                                        | Search String                                      |
|:------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| **DexEvolve**     | Pokémon kept for evolving but for which I do not yet have enough candy, either to further complete the Dex or for randomized evolves (e.g. Tandemous to Maushold Family of Three). | `evolvenew,133,206,236,265,366,420,744,848,924`    |
| **CandyTransfer** | Anything that may be hard to get by (e.g. legendaries) but is otherwise good for transfer, kept for double candy transfer events.                                                  | `count2-&0*,1*,2*&legendary,mythical,ultra beasts` |
| **UpTo50**        | Pokémon one step away from becoming level 50, kept for upcoming quests.                                                                                                            |                                                    |

### 4. Keepers

These tags indicate kept Pokémon, which would otherwise have been transferred or have yet to be transferred or traded. They are colored **black**.

| Tag              | Description                                                                                                                                                 | Search String                                                                                                                                                        |
|:-----------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Regional**     | Anything that can only be found in a specific region, for example Scatterbugs from non-native regions, or Mr. Mime because it is exclusive to Europe.       | `83,115,122,128,214,222,313,314,335,336,337,338,357,369,417,441,455,511,513,515,538,539,550,556,561,626,631,632,664,669,676,701,707,741,749,764,797,798,874,973,978` |
| **KeepOrBetter** | Used when I have a 3 star variant of a Pokémon, but also a different variant which is only 2 stars. Those variants get this tag to avoid being transferred. |                                                                                                                                                                      |
| **Reserved**     | Pokémon reserved for trading with real-life people.                                                                                                         |                                                                                                                                                                      |

## Inbox and Management Search Strings

To keep the collection organized, I use "Inbox" search strings to find Pokémon that fit a category but haven't been tagged yet.
After going through all the inboxes, the `/dev/null` tag is used to transfer any leftover Pokémon that don't fit into any other category.

**Notes**:
- The compact search strings are designed with brackets and have to be passed to a tool like pkgosearch to generate the actual search string.
- `/dev/null` is NOT safe to "Select all" and transfer. 
- ActionInbox does not take the random evolutions into account. This would mean the counter never hits 0.
- ActionInbox also shows new mega evolutions. This is a quirk that can't be solved in PoGo as the `megaevolve` filter only filters on _new_, possible mega evolutions (e.g. those you have enough energy for). I just tag them as DexEvolve or CandyTransfer.

| Name            | Description                                                                                        | Compact Search String                                                                                                                                                                                                                        | Expanded Search String (Usable in Pokémon GO)                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:----------------|:---------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/dev/null**   | The ultimate "trash" filter after going through all inboxes.                                       | `0*,1*,2*&!#&count2-&!favorite&!buddy1-&!@special`                                                                                                                                                                                           | Same as compact                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Dupes**       | Duplicate Pokémon                                                                                  | `count2-`                                                                                                                                                                                                                                    | Same as compact                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **KOBMismatch** | Finds items in the KeepOrBetter tag which might need revising. Will likely never end up hitting 0. | `#KeepOrBetter&count2-`                                                                                                                                                                                                                      | Same as compact                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **ObjInbox**    | Finds untagged Pokémon that match Objective criteria.                                              | `!#Remote Trade&!#Shiny&!#Level 1&!#Hundo&!#Nundo&!#Event/BG&!#Rare&(shiny,cp10,4*,(0attack&0defense&0hp),costume,background,151,251,385,479,480,481,482,490,492,494,647,648,719,721,789,790,791,792,802,803,890,893,999)`                   | `!#remote trade&!#shiny&!#biggest&!#level 1&!#hundo&!#nundo&!#event/bg&!#rare&shiny,cp10,4*,0attack,costume,background,151,251,385,479,480,481,482,490,492,494,647,648,719,721,789,790,791,792,802,803,890,893,999&shiny,cp10,4*,0defense,costume,background,151,251,385,479,480,481,482,490,492,494,647,648,719,721,789,790,791,792,802,803,890,893,999&shiny,cp10,4*,0hp,costume,background,151,251,385,479,480,481,482,490,492,494,647,648,719,721,789,790,791,792,802,803,890,893,999` |
| **StatusInbox** | Finds untagged Pokémon with specific statuses.                                                     | `!#Remote Trade&!#CandyTransfer&!#Mega&!#AdventureEffect&!#DoNotPurify&(mega1-,adventureeffect,(shadow&(68,94,99,123,130,143,145,146,149,150,243,244,248,254,257,260,282,310,319,373,376,382,383,409,461,462,464,466,473,475,530,609,635)))` | `!#remote trade&!#candytransfer&!#mega&!#adventureeffect&!#donotpurify&mega1-,adventureeffect,shadow&mega1-,adventureeffect,68,94,99,123,130,143,145,146,149,150,243,244,248,254,257,260,282,310,319,373,376,382,383,409,461,462,464,466,473,475,530,609,635`                                                                                                                                                                                                                              |
| **ActionInbox** | Finds untagged Pokémon that might need action.                                                     | `(!#DexEvolve&!#CandyTransfer&evolvenew),(!#&((0*,1*,2*)&legendary,mythical,ultra beasts))`                                                                                                                                                  | `!#dexevolve,!#&!#dexevolve,0*,1*,2*&!#dexevolve,legendary,mythical,ultra beasts&!#candytransfer,!#&!#candytransfer,0*,1*,2*&!#candytransfer,legendary,mythical,ultra beasts&evolvenew,!#&evolvenew,0*,1*,2*&evolvenew,legendary,mythical,ultra beasts`                                                                                                                                                                                                                                    |
| **KeepInbox**   | Finds untagged Pokémon that are candidates for keeping or trading.                                 | `!#Remote Trade&!#Regional&83,115,122,128,214,222,313,314,335,336,337,338,357,369,417,441,455,511,513,515,538,539,550,556,561,626,631,632,664,669,676,701,707,741,749,764,797,798,874,973,978`                                               | Same as compact                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
