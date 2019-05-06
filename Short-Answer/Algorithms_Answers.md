Add your answers to the Algorithms exercises here.

1. This while loop evaluates to a < n^3, within each loop we add n^2 to a. So after the first loop, when a = 0 we have n^2, then on the second turn we add n^2 again for a grand total of n^4 which is greater than n^3. No matter the size of n this loop will run twice in the worst case, so we can say that this has O(1) Runtime.

^^This is totally wrong, I messed up my addition of exponents. This will run O(n) times.

2. I'll evaluate this starting with the innermost loop, k + 1 -> 10 + k is really just another way of saying 0 -> 9 so this will evaluate down to a constant. When considering Big O, we can generally ignore constants once n becomes very large, so for our next range j + 1 -> n we can ignore the + 1 and just consider that this loop has a worst case runtime of O(N). We can also extrapolate that our for the two preceeding loops, but since these loops are nested, we multiply our N instead of add them. So we come to a grand total of O(10 \* N^3), but we can generally ignore constants when we are talking about runtime for very large N, so we can simplify our runtime to O(N^3)

3. This runtime is O(N). What happens is that for each n we add to the bunnies function, we add another call to the stack. I.e. for n = 5, we cann bunnyEars 5 times, so there's a direct relation between our Big 0 and the size of our call stack, which determines our runtime.

Exercise II

This is a perfect opportunity to use a binary search. Since floors are ordered in ascending order, we already have a sorted list of values to work off of. So what we should do is choose the midpoint and see if the egg breaks or doesnt break when tossed from that floor, if it doesn't break then we divide the remaining rooms above us in half and move to that point. If it does break, then we move to the midpoint of the rooms below us. We then repeat this process until we find the exact highest floor you can drop an egg from so that it doesn't break.

The runtime of this algo is O(log N). Which means that if we moved from 32 -> 64 floors, it would only take 1 extra move to find the exact floor.
