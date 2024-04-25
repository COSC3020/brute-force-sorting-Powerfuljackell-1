[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/7eEMzrNd)
# Brute-Force Sorting

We talked about the complexity of the sorting problem, and used an argument over
all permutations of a list to be sorted to determine its complexity. Implement
a function to sort a list by systematically trying all permutations of the input
list, using the template in `code.js`. Test your new function; I've provided
some basic testing code that uses [jsverify](https://jsverify.github.io/) in
`code.test.js`.

The return value should be the number of permutations that were tried until the
sorted list was "discovered". The unsorted list passed as an argument should be
sorted, i.e. do not copy the list and sort the copy.

## Runtime Analysis

What is the runtime complexity of the algorithm that you implemented? What does
a best case input for your implementation look like, what does a worst case
input look like? How would this complexity change if you generated permutations
randomly without memory instead of systematically trying them?

The runtime complexity would be O(n!*n) as each value must be iterated over to create a new permutation each time, with each permutation creating a new unique combiniation of the input array, thus, $1 * 2 * 3 * 4 ...$. The additional *n is attributed to the isSorted() function, as it adds an additional check each time an iteration occurs, where it checks each value within the current permutation to see if the given array is sorted. A best case input would be a set of values that is already sorted, as naturally the first permutation is already input first. Worst case is average, as each permutation is just as likely as the other, making my worst case O(n!). If they where truly randomized and not systematically itereated through, AND they did not have repeat checking in place, the worst case could potentially be infinite, as the permutation generator could just go on forever without finding the correct permutation.

Describe your reasoning and the conclusion you've come to. Your reasoning is the
most important part. Add your answer to this markdown file.
