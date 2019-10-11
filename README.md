# Teen Patti

## Elements of the game

### Betting

**Turns:** Turns are played in counter-clockwise direction with the winner of previous
round being designated as the dealer.

**Entry Fee:** Every player has to put in a *minimum* bet in order to join a game. This
ensures that a player playing *tight* game also loses money every round.
~A player temporarily leaving the table has to put up the *Ante* to the pot for the next
round.~

**Blinds:** Blind players put up at least *half* the amount of the current level of bet
by a seen player. We will not implement a *force blind* round after the ante.

**Calling and raising:** A player can call and/or raise the bet by either calling at
least an equal amount that was called before or raising it to a newer amount.
A blind player has to put in a minimum of half the current bet amount.
Betting will continue till each player has matched the current bet or a defined
threshold of number of rounds of betting are matched or peak betting amount is hit.

###


##### Expected Problems ######

**Limiting the raise:** We need to figure out a mechanism to limit

**Resolving "all-in" situations:** The

**Handling players exiting a round:**


A "game" needs to be a series of hands rather than a single hand.
You'll want some sort of structured required bet. Blinds are more interesting than antes.

For this game specifically, it looks really useful to support more than two players.
You should plan allow 2-8 players per table, at least as a stretch goal
