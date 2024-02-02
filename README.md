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

Asymptotic analysis may be misleading for actual performance because it is detailing very large inputs, so a small input size could cause the determining factor of runtime to be one of the constants that gets dropped when performing an asymptotic analysis. An algorithm that has asymptotic complexity of n^5 would be inefficient for inputs of more than 100, but given a single input, the main runtime could actually be controlled be a constant +20 that wouldn't be accounted for in the asymptotic analysis; 100000 log n and 2 log n are both simply log n using this approach. The input could be in the best or worst format for the algorithm, such as recieving an already sorted array for either insertion sort or quick sort, which could vastly change runtime. Additionally, asymptotic analysis assumes a perfect environment, an algorithm optimized for one type of machine or runtime environment may run significantly slower outside of optimized environments. For Example the dual pivot vs single pivot for quicksort in javascript versus python.

Binary search has an average runtime of log(n), so c log_2 (1000) = 5. So c=0.50172. Using the same constant factor c, we have T = 0.50172 log_2(10000) = 6, so about 6 times longer, or 30 seconds total.

A difference like this could be because the tree had the searched for element in the first position, this is the worst case scenario with the algorithm required to go through every single step to find the result. This could also be due to the case with 1000 elements, if the input was formatted for best case scenario, the 5 seconds could be initial operations before the search begun, which would mean the estimation was based on the best case. The algorithm could be inefficient and not scale exactly with log(n), an additional coefficient would be unaccounted for in the analysis, which would drastically increase runtime. If instead the algorithm scaled with n log(n), the smaller input size would run significantly faster than the larger one. With the n factor actually as the dominant term.
