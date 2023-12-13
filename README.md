[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11861567&assignment_repo_type=AssignmentRepo)
# Theory vs. Practice

- List 3 reasons why asymptotic analysis may be misleading with respect to
  actual performance in practice.
  ## Answer
  1. Asymptoic removes the constant factor(c) and lower order which made it misleading. For instance, Tp(n) = 5x^2+100, Tq(n) = 1000000000x^2, they have the same time complexity of x^2. With the same moderate input size x = 1000, Tq(n) runs much slower than Tq(n) which is misleading.
  2. Hardware and Platform Variability: In today's world of computer hardware like memory hierarchies, and parallelism can all affect how well a program runs. Even if you have the same algorithm, it might not work the same on different hardware or if you use different compilers and settings.
  3. When employing asymptotic notation to describe an algorithm's running time, it's crucial to specify which running time we mean. Sometimes we focus on the worst-case scenario, but frequently, our goal is to capture the running time across all possible inputs. In essence, we often seek a general statement that applies universally, not just to the worst-case scenario. As O-notation represents an upper bound, using it to set a bound on the worst-case running time of an algorithm establishes a limit for the running time across all possible inputs. This aligns with the universal statement we previously discussed.

      Technically, labeling the running time of insertion sort as O(n^2) is imprecise, as the actual runtime fluctuates based on the specific input of size n. When we assert "the running time is O(n^2)," we are stating that there exists a function f(n) within the O(n^2) complexity class. This function ensures that, regardless of the chosen input of size n, the running time is consistently upper-bounded by the value of f(n). In essence, this statement is equivalent to expressing that the worst-case running time is O(n^2).


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

get some hints from below website: https://math.stackexchange.com/questions/3359564/what-does-n-0-mean-when-describing-big-o-notation#:~:text=Big%2DO%20notation's%20English%20definition,and%20does%20so%20until%20infinity.
