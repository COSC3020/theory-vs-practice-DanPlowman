[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/FgMJElkj)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

Add your answers to this markdown file.

Answers:

Asymptotic analysis may be misleading for actual performance because it is detailing very large inputs, so a small input size could cause the determining factor of runtime to be one of the constants that gets dropped when performing an asymptotic analysis. The input could be in the best or worst format for the algorithm, such as recieving an already sorted array for either insertion sort or quick sort, which could vastly change runtime. It also gives performance with respect to input values, not actual runtimes.
Binary search has an average runtime of log(n), so log_2 (1000) = 9.96, and log_2 (10000) = 13.29, about a 50% gain, so an estimated runtime of 7.5 seconds.
A difference like this could be because the tree had the searched for element in the first position, this is the worst case scenario with the algorithm required to go through every single step to find the result. This could also be due to the case with 1000 elements, if the tree was formatted for best case scenario, which asymptotically does not scale, the 5 seconds could be initial operations before the search begun, which would mean the estimation was based on bad data. The algorithm could also be inefficient and not scale exactly with log(n), an additional coefficient would be unaccounted for in the analysis, which would drastically increase runtime.
