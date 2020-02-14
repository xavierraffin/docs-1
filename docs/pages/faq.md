---
title: Developer - Frequently Asked Questions
permalink: /faq
subtitle: 
layout: card
---

#### Do I need to know how to program?

Battlesnake is best for those with beginner level programming skills and above. You'll have to know the basics of at least one programming language to get started.

If you're brand new to programming and want to start learning - awesome, we're happy you're here! We're working on some new resources and ways to help you get started. In the meantime, you might want to check out some online programming tutorials to get the basics down.

---

#### Does Battlesnake require machine learning / artificial intelligence?

You can build your snake using any technology you want! It doesn't have to be machine learning or artificial intelligence - in fact, many participants have great success writing simple programs and decision trees. We suggest you start with technologies you're comfortable with and expand to include new things you want to learn.

---

#### What cloud provider and region is play.battlesnake.com hosted in?

The current game engine is hosted on Google Cloud Platform, in the `US-WEST1` (Oregon) region. It's possible, but unlikely this could change in the future. It's more likely that we'll expand the engine to include multiple and configurable regions.

---

#### How does food spawn on the board?

The algorithm that generates food is very simple. Each turn the engine evaluates the board and determines if there is any food. If no food is found, a piece of food will spawn. If food is found, there is a 15% chance that another piece of food will spawn. When food spawns, it will appear in random, open location on the board. If there are no open locations on the board, no food will spawn.

```python
# pseudocode example
chance = 15%
if no food on board:
    chance = 100%
if random(chance):
    spawn food in random empty square
```

If you are interested in the implementation of the algorithm, check out the [Rules](https://github.com/BattlesnakeOfficial/rules) project on GitHub.

---

Have a question that isn't answered? <a href="mailto:hello@battlesnake.com">Let us know.</a>
