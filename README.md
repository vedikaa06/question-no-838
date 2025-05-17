# question-no-838
Solution to the question no 838 on leet code 

838. Push Dominoes
There are n dominoes in a line, and we place each domino vertically upright. In the beginning, we simultaneously push some of the dominoes either to the left or to the right.

After each second, each domino that is falling to the left pushes the adjacent domino on the left. Similarly, the dominoes falling to the right push their adjacent dominoes standing on the right.

When a vertical domino has dominoes falling on it from both sides, it stays still due to the balance of the forces.

For the purposes of this question, we will consider that a falling domino expends no additional force to a falling or already fallen domino.

You are given a string dominoes representing the initial state where:

dominoes[i] = 'L', if the ith domino has been pushed to the left,
dominoes[i] = 'R', if the ith domino has been pushed to the right, and
dominoes[i] = '.', if the ith domino has not been pushed.
Return a string representing the final state.

How it works:
Add virtual dominoes at both ends ('L' at start, 'R' at end) to simplify edge cases.

Find all non-. dominoes and store their positions and symbols.

For each pair of force symbols:

If they are the same (e.g., R...R or L...L), fill the middle with that symbol.

If it's R...L, dominoes fall toward each other from both sides. The middle one stays upright if equidistant.

Efficient:
It processes the dominoes in one pass between each pair, resulting in a fast solution.
