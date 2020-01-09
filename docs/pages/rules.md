---
title: Battlesnake Game Rules
subtitle: Updated October 2019
permalink: /rules
layout: card
---

## What is Battlesnake?

Battlesnake is an autonomous survival game where your snake competes with others to find and eat food without being eliminated. To accomplish this, you will have to teach your snake to navigate the serpentine paths created by walls, other snakes, and your own growing tail without running out of energy.

---

## Winning the Game

Winning is quite simple: be the last snake slithering. But slithering takes health and space –– if you run out of either, you’re eliminated.

#### Health and Movement

At the start of the game, your snake will be placed on the battlefield along with their opponents and everyone will have a full health meter. Every turn, your snake will be asked by the game to pick a direction: up, down, left, or right and, once they respond, they will move exactly one space in that direction. But slithering is hard work and moving that one space will drain your snake of one health.

In order to restore that health, your snake needs to find and eat the traditional food of snakes: brightly colored circles. On the turn your snake’s head enters the space with the nutrition disc, they will immediately consume it, resetting their health to maximum and increasing their length by one – one of many good reasons not to follow other snakes too closely (the view from there’s not great, either).

#### Space

Snakes need more than just food to survive, they need space to roam and be free. However, in Battlesnake, space is limited. Every turn, your snake has to move into a new space, but so does every other snake. As all snakes grow, finding the best path through the remaining spaces gets harder and harder.

Most importantly, the Battlesnake arena is surrounded by boundary walls –– any snake attempting to sneak over one of these walls will be eliminated.

#### Snake-on-Snake Contact

Battlesnake is a battle of wits and honor. Snake-on-snake contact is only allowed when two snakes meet head-to-head. If your snake attempts to bite any snake’s body, including its own, it will be eliminated for unsport-snakelike conduct. When two snakes do meet head-to-head, the outcome is simple: the big snake stays, the little snake goes, so make sure your snake’s eyes aren’t bigger than its stomach.

---

## The Battlesnake Arena

Battlesnake is played on a rectangular board of variable size, with up to 8 total snakes. At the beginning of the game, there will be one piece of food for each snake doing battle. Subsequent food will be placed randomly on the board according to a Super Secret Proprietary Algorithm*. In games with many snakes, multiple pieces of food may appear in a single turn.

To eat a piece of food, your snake must move into the space that contains the food, this includes losing one health and fending off any other snakes that want to move into that space that turn. Consuming food costs no health, so a snake can eat when at 0 health and be rejuvenated in time to keep moving on the next turn.

_* the algorithm is neither secret nor proprietary, but it is arguably super. See it for yourself at [github.com/battlesnakeofficial/engine](https://github.com/battlesnakeofficial/engine)_

#### Game Start

Each snake starts out occupying a single space (turn 0) and will grow for the first two turns as it slithers into the arena.

---

## Programming Your Snake

Battlesnake is more than a game of snakes and nutritious floating orbs, it’s also about people and how they program those snakes. So it’s useful to understand exactly what happens during each turn.

__Each turn in a Battlesnake game is divided into 3 parts:__

#### 1) The Battlesnake server sends board information to every snake.

The game server will send to each snake, in parallel, a /move request with information about the current state of the game board. This gamestate includes the location of every piece of food on the board as well as the health of all snakes and the spaces they occupy. There is also some meta information about the game, like an id, turn #, and board dimensions for those Bobby Fischer snakes out there playing multiple games at once.

#### 2) Each snake responds with their move.

After receiving information about the board, each snake has to respond with a move of "up", "down", "left", or "right" within the allowed timeout period. You can find more specific details on what this response should look like in the [Official Snake API](https://docs.battlesnake.com/snake-api). If your snake’s cybernetic brain fails to provide a valid response in time, instinct kicks in and they will continue moving in the same direction as the previous turn (on the first turn, this defaults to up) even if it means certain doom.

#### 3) Turn resolution.

At the end of the timeout period (or as soon as all snakes have responded with a move), the Battlesnake server will resolve all snake movements and update the board and snake statuses accordingly. This happens in a very specific order:

1. Each snake will have their health reduced by one.
2. Each snake will have a new body part added to the board in the next space in their chosen direction. This will be their new head.
3. Each snake will have their last body part (their tail) removed from the board.
4. Any snake that's found a nutrition disc gets to eat:
  * Snakes that have eaten food have their health reset to maximum.
  * Snakes that have eaten food this turn receive an additional body part placed on top of their current tail. This will extend their visible length by one on the next turn.
  * Eaten food is removed from the board.
5. Any snake that runs into a wall, another snake, or itself will be eliminated and removed from the board. They will have their status updated and will be notified with an /end request (no response necessary).
6. Potentially a new piece of food will be placed on the board, according to game parameters and food spawn algorithm.
7. If there are at least two snakes still slithering, proceed to the next turn. Otherwise inform the remaining snake of its victory with an /end request and end the game.
