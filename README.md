# Teen Patti

*Teen Patti* (Hindi for Three Card Poker) is a well game known and played in the Indian
sub-continent region. Essentially, every player is given a hand of 3 cards
We plan to build an web version of the game that's compatible with mobile devices as well.

The rules of Teen Patti usually vary and are agreed upon before the match. Ranking of
cards are pretty well established and common. Below are definitions for some of the
varying rules for our implementation:

**Entry Fee:** Every player has to put in a *minimum* bet in order to join a game. This
ensures that a player playing *tight* game also loses money every round.

**Blinds:** Blind players put up at least *half* the amount of the current level of bet
by a seen player. We will not implement a *force blind* round after the ante.

**Calling and raising:** A player who has seen the cards can *call* by the minimum amount
or *raise* the bet. A blind player will have to *call* or *match* half of the minimum
calling amount. When a blind player *raises* the bet, every *seen* player has to *call* a
minimum of the double the blind bet.

**A Game:** A game will be made up of 5 rounds.

**Limiting:** Tables will have a *spread-limit* for a total maximum bet on the table.

**Side-show:** A player can request the previous player for a (side-)show by putting up
double the minimum bet amount and if accepted, they participate in a private *show* of
hands. A blind player __cannot__ request for side-show.

**Show:** When only two players are playing, any player can request for show of cards, by
putting double the minimum bet amount.

### Stretch Goals

**Number of players:** Objective is to allow up to 8 players on a table.

**Variations of Teen-Patti:** Have different tables running different variations of Teen-
Patti, namely, *Best-of-four* and *Community*.
