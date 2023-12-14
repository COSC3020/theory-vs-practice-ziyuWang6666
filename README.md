[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11861567&assignment_repo_type=AssignmentRepo)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  ## Answer
  1. Asymptoic removes the constant factor(c) and lower order which made it misleading. For instance, Tp(n) = 5x^2+100, Tq(n) = 1000000000x^2, they have the same time complexity of x^2. With the same moderate input size x = 1000, Tq(n) runs much slower than Tq(n) which is misleading.
  2. Hardware and Platform Variability: In today's world of computer hardware like memory hierarchies, and parallelism can all affect how well a program runs. Even if you have the same algorithm, it might not work the same on different hardware or if you use different compilers and settings.
  3. Only $\Theta$-notation accurately represents a tight bound. $O$ and $\Omega$-notation are loose bound. The asymptotic upper bound offered by O-notation may or may not precisely characterize the growth rate. For instance, the bound $2(n^2)$ = $O(n^2)$ is asymptotically tight, but the bound 2n = $O(n^2)$ is not. Consider the insertion sort's best-case running time, denoted as $\Omega(n)$ instead of $\Omega(n^2)$ because it occurs when the input list is already sorted. On the other hand, the worst case for insertion sort is $O(n^2)$. Consequently, the running time of insertion sort falls within both $\Omega(n)$ and $O(n^2)$, revealing a lack of tight bound precision that can be misleading.--from textbook


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
  2. Some important considerations include input distribution and implementation-specific factors. Variations in runtime may arise when the arrangement or distribution of elements in the input deviates from the average or expected case assumed by asymptotic analysis. Furthermore, observed runtimes can be influenced by the efficiency of the algorithm's actual implementation, encompassing factors such as hardware dependencies, compiler optimizations, and other implementation-specific details.
  3. There may be an element at the bottom of the tree you want to search for, but the tree is skewed. Or 20% of the programming runs on Windows machine while 80% runs on a Pi.

Add your answers to this markdown file.

get some hints from below website: https://math.stackexchange.com/questions/3359564/what-does-n-0-mean-when-describing-big-o-notation#:~:text=Big%2DO%20notation's%20English%20definition,and%20does%20so%20until%20infinity.
