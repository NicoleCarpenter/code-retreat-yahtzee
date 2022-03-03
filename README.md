# Code Retreat

Today we will be having fun and writing some code! We are going to write a solution to a coding challenge in the language of your choice. The game we will be programming today is [Yahtzee](https://www.youtube.com/watch?v=sQM7sN4NPz8).

![Yahtzee](https://www.ultraboardgames.com/img/slideshow/yahtzee.jpg)

## Gameplay

Yahtzee is a dice game played with five dice that plays similar to poker. For each player's turn, they can roll the dice up to three times and they can roll as many dice as they wish.

Typically after the first roll, the player will decide which die to re-roll based on what item on the score card they are targeting. Each line item can only be used once per game (with the exception of the Yahtzee bonus which will be described later).

![Yahtzee scorecard](https://images-na.ssl-images-amazon.com/images/I/51MI73wpG-L._SX331_BO1,204,203,200_.jpg)

The score card will include the following sections

### Top Section

The top section is a count of all die of a particular number. The score is the count of only the number you are targeting. For instance, if you are rolling for fours and you got [4, 4, 4, 5, 1], your score on the 4's line would be 12.

- 1's
- 2's
- 3's
- 4's
- 5's
- 6's

If you average 3 or more of each of the above items, you are rewarded a bonus of 35 points.

### Bottom section

The bottom section contains score values for particular poker-like scenarios. These items have different scoring rules.

- 3 of a kind - At least 3 dice with the same value, count total of all die
- 4 of a kind - At least 4 dice with the same value, count total of all die
- Full house - 2 of one value, 3 of another, 25 points
- Small straight - 4 consecutive numbers ie: [1, 2, 3, 4, 1], 30 points
- Large straight - 5 consecutive numbers ie: [1, 2, 3, 4, 5], 40 points
- Yahtzee - 5 of a kind
- Chance - Total of all dice

### Bonus Yahtzee

If you happen to get luck and hit Yahtzee more than once, you would mark a Yahtzee Bonus space for each additional Yahtzee achieved. Each Yahtzee Bonus is worth 100 points.

If you hit a Yahtzee Bonus, you would also fill out another line above that is applicable to the die you rolled. For example, if you rolled [5, 5, 5, 5, 5], you can mark the following options

- 25 points in your 5 space
- 30 points for 3 of a kind
- 40 points for 4 of a kind
- 25 points for chance
- 0 points for any other space

### Additional strategy

You can mark 0 in any space for any turn if you don't have a good move to make and you have either already used your chance or you don't want to use it for that roll.

## Milestones

For this challenge, we will be looking to hit several milestones on the way to getting a working version of Yahtzee. Let your host know when you have hit each milestone.

1. roll one dice
2. roll 5 dice
3. reroll all dice
4. reroll some dice
5. count total value on all dice
6. count total value on select dice
7. display a score card
7. mark a score card
8. play a game
9. end a game

## Stretch Goals

1. multiple players
2. automatically recognize best move for current roll
3. automatically recognize best move for current roll considering current score card
4. suggest possible options for best move on next roll
5. suggest possible options for best move on next roll considering current score card

## Installation

Choose the language you wish to work on and set up your environment. For the purposes of this workshop, we are going to assume that you are using either Ruby, Python, or JavaScript. While creating the application using a framework may be overkill (ie: Rails or Django), you are welcome to use one if it is easier for you.

To get started, create a directory for our game

```ruby
mkdir yahtzee
cd yahtzee
```

## Tests

Please choose a language with a testing tool that you are familiar with.

#### Ruby

With Ruby, the most common testing tool is [rspec](https://github.com/rspec/rspec-rails), but [minitest](https://github.com/seattlerb/minitest) is another option. You can install these by including the respective gem in a Gemfile.

```ruby
# Gemfile
source "https://rubygems.org"

gem "minitest"
gem "rspec"
```

Then simply bundle your project to install the dependencies

```ruby
bundle install
```

#### Python

[unittest](https://docs.python.org/3/library/unittest.html) is a testing framework included in python's standard library, meaning you can simply include the module in your test file

```
import unittest
```

Another popular option is [pytest](https://docs.pytest.org/en/7.0.x/). You can install pytest using pip.

```python
pip install pytest
```

#### JavaScript

For JavaScript, [jest](https://jestjs.io/) is typically the go-to option. Jest can be installed using yarn

```javascript
yarn add --dev jest
```

Or npm:

```javascript
npm install --save-dev jest
```
