[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11861567&assignment_repo_type=AssignmentRepo)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  ## Answer
  1. Asymptotic is just meaning growth this way, it's a kind of change.
  Also, it removes the constant factor, it doesn't mean the exact number.
  2. Hardware and Platform Variability: In today's world of computer hardware things like CPUs, memory hierarchies, and parallelism can all affect how well a program runs. Even if you have the same algorithm, it might not work the same on different hardware or if you use different compilers and settings.
  3. Cannot make inferences between different cases in general. The best case does not equal Omega, the worst case does not mean the performance is big O, and the average case does not indicate it performs as Theta.

- Suppose finding a particular element in a binary search tree with 1,000
  elements takes 5 seconds. Given what you know about the asymptotic complexity
  of search in a binary search tree, how long would you guess finding the same
  element in a search tree with 10,000 elements takes? Explain your reasoning.

  ## Answer
  A binary search tree's avergae time complexity is O(logn), because O(log1000 base 2)=10 seconds.
  So it will take O(log10,000 base 2)=14 seconds.

- You measure the time with 10,000 elements and it takes 100 seconds! List 3
  reasons why this could be the case, given that reasoning with the asymptotic
  complexity suggests a different time.

  ## Answer
  1. The computer hardware may not be optimized.
  2. It's possible that the input data is poorly organized, causing the algorithm to behave poorly, resulting in O(nlog2(10,000)).
  3. Although constant and low-order terms are not factored into the algorithm, they can significantly impact the actual running time in practice.

Add your answers to this markdown file.
