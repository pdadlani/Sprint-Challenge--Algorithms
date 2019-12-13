#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n): each iteration of the loop keeps adding n**2 to the value, until the value reaches n * n * n. This will happen only n number of times.


b) O(n log(n)): the for loop goes through n iterations, while the inner while loop goes through log(n) iterations, as the value of the parameter j is being doubled each time.


c) O(n) where n is length of bunnies: the function makes n recursive calls to itself, with each call taking constant amount of time.

## Exercise II

n-story building with plenty of eggs. eggs can get broken if thrown off floor f or higher. Solution to find the highest floor where no eggs will break:

1. let minFloor = 0, maxFloor = n
2. get mid point of minFloor and maxFloor
3. throw egg of mid point
  a. if it breaks, change maxFloor to mid point, and repeat steps 2 and 3
  b. if it does not break, change minFloor to mid point, and repeat steps 2 and 3
4. if egg breaks from one floor above current floor and does not break at current floor, return current floor number

def whereEggBreaks(n):
  minFloor = 0
  maxFloor = n

  def test(minFloor, maxFloor):
    midPoint = middle of minFloor and maxFloor

    if minFloor + 1 == maxFloor:
      return current floor number

    if egg breaks from midPoint:
      maxFloor = midPoint
      test(minFloor, maxFloor)
    else:
      minFloor = midPoint
      test(minFloor, maxFloor)