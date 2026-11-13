# Slay the Spire II AI
Hannah Storer, Sam Pollak, Alan Tai

We built and trained three AI agents (Expectimax, Monte Carlo Tree Search, and Q-Learning) to play Slay the Spire II (STSII) with the goal of optimizing the first fight of the game to minimize HP lost. Slay the Spire II is a rogue-like deck building video game where you play as a character, battling enemies in card based combat in order to progress through a Spire. You start with a deck of basic cards and acquire additional cards and items after each fight. You battle enemies through strategic combat, choosing your moves based on player stats (HP, block, energy), enemy stats (HP, enemy intent for next move, block, strength). The fights in the game get progressively harder as you progress. Here, we compared how three AI agents we built and trained perform in the first fight.

## Simulating Slay the Spire II in Terminal

We built a full card-battler engine with classes and mechanics that directly reflect STSII. The terminal interface allows the player to play the fight interactively against enemies that behave directly like in STSII with predicted behavior and mirroring statistics. This can be played with playgame.py. We used this simulation to train our models.

Gameplay:
1. Pick a character via the numbered character selection
2. Pick an enemy via the numbered enemy selection
3. Each turn shows the current state of the game with player HP/Block/Energy, enemy HP/Block/Strength, the enemy's next move, and the player's current card hand. Type a card number to play the card or type "end turn" to end the player turn and start the enemy turn.
4. The game repeats until either the player or the enemy reaches 0 HP.

## Our Algorithms and Results

For all performance tests we evaluated the algorithms with 1000 fights. Additionally, we compared our algorithms to a random choice baseline. Here are the results of how our algorithms performed in terms of mean HP lost.

Random Choice Baseline: 44.1
Expectimax: 7.4
Q-Learning: 8.3
Monte Carlo Tree Search: 9.1

All three of our algorithms performed much better than the Random Choice Baseline. Expectimax performed the best with only an average of 7.4 HP lost in the first fight.
