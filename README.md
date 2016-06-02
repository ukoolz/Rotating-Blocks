# Rotating-Blocks

Rotating Blocks:

There are seven blocks, with the numbers 1 to 7 printed on them, and they are

placed in a row. The order of the blocks can be changed by four different

operations; in each case removing one of the blocks, pushing three of them along

the row to make a gap, and then placing the removed block back in the gap

created.

Only 4 operations are allowed:

1. LEFT_TO_MID

The leftmost block is temporarily removed and the adjacent three blocks

pushed left.

2. RIGHT_TO_MID

The rightmost block is temporarily removed and the adjacent three blocks

pushed right.

3. R_LEFT_TO_MID

First reverse the string and then apply LEFT_TO_MID operation.

4. R_RIGHT_TO_MID

First reverse the string and then apply RIGHT_TO_MID operation.

For example, suppose that the blocks were in the order 1234567.

The first operation would change the order to 2341567.

The second would change it to 1237456.

The third to 6547321.

And the fourth to 7651432.

Given the starting order of the blocks we are interested in finding the smallest number of

operations that are required to change the order to 1234567.

Determine the smallest number of operations to change a given order to 1234567.

Algorithm:

The algorithm applies BFS on tree until it reaches goal state, you have to maintain the

level of the state you are going to process. If current state of string matches with goal

state then level of that state will be the minimum number of operations required to reach

goal state.

Input:

1. Initial configuration:

An integer array of size 7 which contains the numbers 1-7 in some order.

2. Goal configuration:

Another integer array of size 7 which contains the numbers 1-7 in some

order.

3. A set of operations:

An integer array of size maximum 10 which stores a set of operations.

Numbers 1-4 define the following operations.

1 -> LEFT_TO_MID

2 -> RIGHT_TO_MID

3 -> R_LEFT_TO_MID

4 -> R_RIGHT_TO_MID

Output:

You need to implement the following functions:

1. Separate functions for the 4 rotation operations which take an array as input

and return the modified array (do not overwrite the original).

The prototypes are given below:

int* left_to_mid(int *a);

int* right_to_mid(int *a);

int* r_left_to_mid (int *a);

int* r_right_to_mid (int *a);

2. Goal configuration reached after following a set of operations.

The function takes an initial configuration and an array of operations and prints

the goal state.

The prototype is given below:

void return_goal(int *initial, int *operation);

3. Breadth first search.

Use a recursive implementation of BFS to reach from an initial configuration to

the goal configuration in minimum number of steps possible.The function prints

the minimum number of steps required.

Test Case:

Input:

Output:

7 6 5 2 1 4 3 (initial)

1 2 3 4 5 6 7 (goal)

1 4 (set of operations)

3 4 1 6 7 2 5 (goal state reached after following the set of operations)

2

R_ LEFT_TO_MID

LEFT_TO_MID
