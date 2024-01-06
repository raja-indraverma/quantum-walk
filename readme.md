# for 1-D random walk

## Probability Distribution:
prob = [0.05, 0.95]: This defines the probabilities of moving down and up, respectively. In this case, there's a 5% chance of moving down (to the left) and a 95% chance of moving up (to the right).

## Initial Position:
start = 2: The starting position for the random walk is set to 2.

## Random Walk Simulation:
rr = np.random.random(1000): Generates an array of 1000 random numbers between 0 and 1.
downp = rr < prob[0]: Creates a boolean array where elements are True if the corresponding element in rr is less than 0.05.
upp = rr > prob[1]: Creates a boolean array where elements are True if the corresponding element in rr is greater than 0.95.

## Iterating Through Random Steps:
The code iterates through each pair of boolean values in downp and upp.
If the current position allows, it either moves down or up based on the generated random numbers.
The updated position is then appended to the positions list.


# for 2-D random walk

## Number of Steps and Arrays Initialization:
n = 100000: Specifies the number of steps in the random walk.
x = numpy.zeros(n): Initializes an array x with n elements, all set to 0.
y = numpy.zeros(n): Initializes an array y with n elements, all set to 0.

## Random Walk Generation:
```
filling the coordinates with random variables
for i in range(1, n):
    val = random.randint(1, 4)
    if val == 1:
        x[i] = x[i - 1] + 1
        y[i] = y[i - 1]
    elif val == 2:
        x[i] = x[i - 1] - 1
        y[i] = y[i - 1]
    elif val == 3:
        x[i] = x[i - 1]
        y[i] = y[i - 1] + 1
    else:
        x[i] = x[i - 1]
        y[i] = y[i - 1] - 1
```
A loop iterates from 1 to n, generating a random integer (val) between 1 and 4.
Depending on the value of val, the walker moves in one of the four directions:
If val is 1, move one step to the right (increase x-coordinate).
If val is 2, move one step to the left (decrease x-coordinate).
If val is 3, move one step up (increase y-coordinate).
If val is 4, move one step down (decrease y-coordinate).
The new x and y coordinates are updated in each iteration.