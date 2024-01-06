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
