# Shiba

There are two ways to use Shiba:

- In private messages
- In the spam channel

In order to use Shiba in private messages, first add Shiba as a friend by going to its [profile page](https://moneypot.com/user/Shiba) on MoneyPot and then clicking the "Add to friends" button. Then, select Shiba from the list of chat channels at right of chat. Now you can send your commands directly to Shiba.

Alternatively, you can use the public "spam" chat channel. First, click the plus button at the bottom right of chat, then select the [spam channel's flag](https://imgur.com/qpgpfsS). To send Shiba commands in the spam channel, prefix them with `!` or `#`.

## Commands

#### balance

Displays your balance with Shiba.

#### rain

`rain <number of players> <amount>`

Shares bits with players from chat chosen at random. Can be used in public channels only.

**Example**: `!rain 5 100` to rain 100 bits each on 5 players for a total of 500 bits.

#### rainon

`rainon <player> <amount>`

Rains on a specific player. To withdraw from Shiba, use the `withdraw` command instead. Can be used in public channels only.

**Example**: `!rainon Ryan 100` to rain 100 bits on the player Ryan.

#### stats

`stats [player]`

Shows a player's rain stats. If no player is given, shows your own stats. The stats only account for random rain, i.e. rain given with the `rain` command but not the `rainon` command.

#### withdraw

`withdraw <amount>`

Withdraw the given number of bits from your Shiba balance to your MoneyPot account.

### Miscellaneous

#### block

Displays when the last Bitcoin block was mined and notifies you when the next one is mined.

#### convert

`convert <amount> <unit> <source currency> [target currency]`

Converts between Bitcoin and various fiat currencies. If no target currency is given, the amount is either converted to Bitcoin or U.S. dollars.

**Example**: `!convert 1.234 BTC JPY` to convert 1.234 Bitcoin to Japanese Yen

#### fair

Shows a link to an explanation of MoneyPot's provable fairness.

#### help

Shows a link to this document.

#### lick

`lick <player>`

Licks another player.

#### seen

`seen <player>`

Shows when a player was last seen in chat.

#### prob

`prob [modifier] <multiplier>`

Calculates the probability of a roll being equal to, greater than or lower than the given multiplier. The modifier can be any of the following:

- =
- \>
- \>=
- <
- <=

**Example**: `!prob >= 2` to calculate the probability of the game ending at or above 2x.

`prob <multiplier> [modifier] x [modifier] <multiplier>`

Calculates the probability of a roll being in between the bounds specified by `x`. The modifier can be any of the following:

- \>
- \>=
- <
- <=

**Example**: `!prob 5 < x < 10` to calculate the probability of the game ending above 5x and below 10x.

#### urban

`urban <term>`

Searches Urban Dictionary for a term.

#### average

`average <duration>`

Calculates the average multiplier for the given duration. Duration can be either a number of games or a duration using any of the following modifiers:

- year
- month
- week
- day
- hour
- minute
- second

To calculate multiple results, pass a comma-separated list of games or durations.

**Example**: `!average 10, 100, 1000` to show the average multipliers over the last 10, 100 and 1,000 games.

#### bust

`bust [modifier] <multiplier>`

Shows the last game which ended at, above or below the given multiplier. The modifier can be any of the following:

- =
- \>
- \>=
- <
- <=

**Example**: `!bust >= 2` to show the last game that ended at or above 2x.

`bust <multiplier> [modifier] x [modifier] <multiplier>`

Shows the last game which ended at a multiplier in between the bounds specified by `x`. The modifier can be any of the following:

- \>
- \>=
- <
- <=

**Example**: `!bust 15 > x > 10` to calculate the last game that ended above 10x and below 15x.

#### median

`median <duration>`

Calculates the median multiplier for the given duration. Duration can be either a number of games or a duration using any of the following modifiers:

- year
- month
- week
- day
- hour
- minute
- second

To calculate multiple results, pass a comma-separated list of games and/or durations.

**Example**: `!median 10` to calculate the median over the last 10 games.

#### nyan

Shorthand for `!bust >= 1000`.

#### profit

`!profit <player> <duration>`

Calculates a player's profit for the given duration. Duration can be either a number of games or a duration using any of the following modifiers:

- year
- month
- week
- day
- hour
- minute
- second

`!profit Leo <duration>` returns the commission earned by MoneyPot itself and `!profit investors <duration>` returns the bankroll investors' profit.

**Example**: `!profit Ryan 100` to show the profit of the player Ryan in the past 100 games.

**Example**: `!profit investors 1month` to show the bankroll investors' profit over the past month.

#### streak

`streak [length] [modifier] <multiplier>`

Looks for the last occurrence of a streak of the given multiplier with at least that length if a length was provided. If no length is provided, looks for the longest streak of the given multiplier.

The modifier can be any of the following:

- =
- \>
- \>=
- <
- <=

**Example**: `!streak 2 >= 1000` to search for the last streak of at least two multipliers at or above 1,000x.

**Example**: `!streak < 2` to search for the longest streak below 2x.

#### wagered

`wagered [player] <duration>`

Calculates how much a player has wagered in the most recent duration. If the player is omitted, the total wagered by all players combined is calculated instead. The duration can be either a number of games or a duration using any of the following modifiers:

- year
- month
- week
- day
- hour
- minute
- second

#### house edge

`he <duration>`

Calculates the average house edge for the given duration. Duration can be either a number of games or a duration using any of the following modifiers:

- year
- month
- week
- day
- hour
- minute
- second

To calculate multiple results, pass a comma-separated list of games or durations.

**Example**: `!he 10, 100, 1000` to show the average house edge over the last 10, 100 and 1,000 games.

#### colors

`colors <duration>`

Calculates the number and percentage of red and green rolls for the given duration. Duration can be either a number of games or a duration using any of the following modifiers:

- year
- month
- week
- day
- hour
- minute
- second

To calculate multiple results, pass a comma-separated list of games and/or durations.

**Example**: `!colors 1k` to calculate the color distribution over the last 1,000 games.

### Moderators

#### automute

`automute <regular expression>`

Instructs Shiba to automatically mute players that post messages matching the regular expression. Does not apply in the spam channel.

#### custom

`custom <player> <message>`

Sets a custom lick message for a player (see lick command).
