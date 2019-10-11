# Teen Patti

*Teen Patti* (Hindi for Three Card Poker) is a well game known and played in the Indian
sub-continent region. Essentially, every player is given a hand of 3 cards, and they bet
whether they have the strongest hand. Strong hands are determined, based on the ranking of
 hands:

 - **Three of kind (trio):** Three same cards, with three Aces being the highest and three
  2s being the lowest.
 - **Straight flush:** Three consecutive cards of the same suit.
 - **Straight sequence:** Three consecutive cards, not from the same sequence.
 - **Color flush:** Three cards from the same suit. Ties are resolved by the first high
 card. If all card values are same, then suits are ranked from Spades > Diamond > Heart >
 Clubs.
 - **Pair:** Two cards of the same value. Pair with higher rank dominates. If a tie still
 exists, then the value of third card decides decides the winner. In the game is still
 tied, ranking of suits determines the winner ( Spades > Diamond > Heart > Clubs ).
 - **High card:** First card with highest value determines the winner. If the game is
 tied, then ranking of card suit determines the winner ( Spades > Diamond > Heart > Clubs
    ).

Below are definitions for some of the varying rules for our implementation:

**Entry Fee:** Every player has to put in a minimum bet in order to join a game. This
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

**Timeout:** A player not playing for 30 seconds will be timed-out to a the minimum bet.
After 3 such timeouts, the player will be removed from the table.

### Stretch Goals

**Increase interactivity:** Increase the interaction between users apart from chats. Maybe
 the ability to gift *items* to other users on the table?

**Incorporate security tests:** Have Static Application Security Testing (SAST) and
Dynamic Application Security Testing (DAST).

**Number of players:** Objective is to allow up to 8 players on a table.

**Variations of Teen-Patti:** Have different tables running different variations of Teen-
Patti, namely, *Best-of-four* and *Community*.

### Challenges for the game:

1. Developing a *structure* for storing information about players and game on the server
is challenging as there is no database to keep track of it. Maintaining the game state for
 each table, with their chat history could require some smart designing on the Elixir side
 of things. Interestingly, we have to develop the ability to *side-show* - a private show
 of cards between two users.

2. Figure which is more interesting - Antes or Blinds: We want to keep the game
interesting and at the same time have a good amount of interactivity from the users. We
intend to take a call between having *forced-blinds* after the Antes for entry, or simply
allowing users to continue play after the Antes. In our experience, *side-show* and blinds
are the elements that keep the game lively, even without the *forced-blinds* round.
