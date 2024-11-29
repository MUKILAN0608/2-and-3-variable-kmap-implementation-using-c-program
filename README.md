This program is designed to simplify Boolean expressions using the Karnaugh Map (K-map) method. It works for expressions involving 2 and 3 variables.

The K-map method helps in reducing Boolean functions by visually grouping 1's in a truth table and finding the minimal expression. This implementation supports:

2-variable K-map: A 2x2 grid used for expressions with two variables.
3-variable K-map: A 2x4 grid used for expressions with three variables.
The program accepts the minterms (the 1's in the truth table) as input and then simplifies the Boolean expression corresponding to those minterms.

How it works:
Input: The user enters the minterms (the positions where the function is true) as a set of values.
For 2 variables, there are 4 possible minterms (m0 to m3).
For 3 variables, there are 8 possible minterms (m0 to m7).
Process: The program maps the minterms onto the K-map grid, finds the largest groups of 1's, and simplifies the expression based on those groups.
Output: The program outputs the simplified Boolean expression.
