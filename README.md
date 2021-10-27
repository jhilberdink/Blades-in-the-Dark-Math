

# Blades-in-the-Dark-Math

The roleplaying game [Blades in the Dark](https://bladesinthedark.com/) uses a dice pool mechanic in which players roll a number of six-sided dice and take the highest result to determine the outcome of their action. In this [jupyter notebook](BitD_Math.ipynb), I calculate the probabilities for different dice pool sizes.

### The Action Roll

The Action Roll is the core mechanic in Blades. The player rolls a number of D6s equal to their character's action rating. If the character has zero in the relevant action rating, the player rolls 2D6 and takes the lower result. The highest die determines the outcome:

- 1-3 is a Failure
- 4-5 is a Mixed outcome; a success that comes with a complication
- 6 is a Success
- If you roll two 6s it's a Critical Success

The following table shows the probabilities for zero to seven dice:

| Dice | Failure | Mixed | Success | Critical |
| ---: | :------ | :---- | :------ | :------- |
|    0 | 75%     | 22%   | 3%      | 0%       |
|    1 | 50%     | 33%   | 17%     | 0%       |
|    2 | 25%     | 44%   | 28%     | 3%       |
|    3 | 12%     | 45%   | 35%     | 7%       |
|    4 | 6%      | 42%   | 39%     | 13%      |
|    5 | 3%      | 37%   | 40%     | 20%      |
|    6 | 2%      | 32%   | 40%     | 26%      |
|    7 | 1%      | 27%   | 39%     | 33%      |

A plot of the action roll results:

![](Resources/Action.png)

At seven dice, a Critical Success becomes more likely than a Mixed Success.

### The Resistance Roll

The Resistance Roll in Blades uses the same dice pool mechanic to determine how much stress a character takes when resisting a negative outcome. The character takes 6 stress minus the result of the highest die in their pool. If the player rolls two 6s, they instead recover 1 stress. Again, zero dice means rolling 2D6 and taking the lower result. The table below shows the probabilities for resistance rolls using zero to five dice.

| Dice | 5    | 4    | 3    | 2    | 1    | 0    | -1   |
| ---: | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
|    0 | 31%  | 25%  | 19%  | 14%  | 8%   | 1%   | 0%   |
|    1 | 17%  | 17%  | 17%  | 17%  | 17%  | 17%  | 0%   |
|    2 | 3%   | 8%   | 14%  | 19%  | 25%  | 28%  | 3%   |
|    3 | 0%   | 3%   | 9%   | 17%  | 28%  | 35%  | 7%   |
|    4 | 0%   | 1%   | 5%   | 14%  | 28%  | 39%  | 13%  |
|    5 | 0%   | 0%   | 3%   | 10%  | 27%  | 40%  | 20%  |

Resistance Roll results visualized on a stacked bar chart:

![](Resources/Resist.png)