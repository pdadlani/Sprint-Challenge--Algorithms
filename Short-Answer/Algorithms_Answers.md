#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n) - the while loop runs up until values of a reach n * n * n (n^3), but inside, a grows by n * n (n^2) each time.

b) O(n logn) - for loop that has a time complexity of O(n) with a nested while loop that runs O(logn) times.

c) O(n) - where n is equal to value of bunnies. This function executes its if statement in O(1) with n recursive calls.

## Exercise II

Given that a building has n floors, and one is searching for floor f where f is the first floor where, if an egg is thrown off, it breaks and will continue to break at any floor between f and n.

To find floor f, you want to start in the middle, with ground being lowest and n being highest floor. Go to the middlemost floor, throw an egg, see the result.

Now you have two options.

1. If it breaks, then your new highest is the middle. Find the middlemost floor between lowest and highest. Repeat your search by calculating the new middle, and test whether the egg will break.

2. If it did not break, then your new lowest is middle. Find the middlemost floor between f and highest. Repeat your search by calculating the new middle, and test whether the egg eill break.

Keep repeating (making these recursive calls) to your function until you find floor f - the lowest floor where an egg will break if thrown off the building. This will happen when:
- an egg thrown off floor f breaks
- an egg thrown off floor f-1 does not break

This is a binary search, therefore O(logn) runtime complexity.
