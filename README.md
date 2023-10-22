[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11861567&assignment_repo_type=AssignmentRepo)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  ## Answer
  1. Asymptotic is just meaning growth this way, it's a kind of change. Also, it removes the constant factor(c) and lower order, it doesn't mean the exact number. Because as n goes to infinte large, the constant factor and lower order are not affect too much. But when the input size is small, 10000*n runs much slower than n, even though they have the same asymptotic analysis(n), which can be misleading.
  2. Hardware and Platform Variability: In today's world of computer hardware like memory hierarchies, and parallelism can all affect how well a program runs. Even if you have the same algorithm, it might not work the same on different hardware or if you use different compilers and settings.
  3. n0 must reach a certain number of n

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  ## Answer
  A binary search tree's avergae time complexity is O(logn).
  For, $T(n)\leq cf(n), \forall n \geq n_0$.
  
  When 5s=c* $\log_{2}1000$, c = 1/2sec.
  
  When 1/2* $\log_{2}10000$ around 6.64 seconds. So it will take around 6.64 seconds.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

  ## Answer
  1. The computer setup is not very powerful.
  2. When searching for a specific element in a binary search tree, the partially unbalanced tree may require searching through multiple nodes before finding the desired element.
  3. There may be an element at the bottom of the tree you want to search for, but the tree is skewed. Or 20% of the programming runs on Windows machine while 80% runs on a Pi.

Add your answers to this markdown file.
