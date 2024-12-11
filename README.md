# Mergesort

Implement an iterative (no recursive calls) and in-place version of mergesort.
Use the template I've provided in `code.js`. Test your new function; I've
provided some basic testing code that uses
[jsverify](https://jsverify.github.io/) in `code.test.js`.

Hint: To make merge sort in-place, think about what happens during the merge --
where are elements moved to and from? To make it iterative, think about the
part of the array each recursive call considers.

## Runtime Analysis

Analyse the time complexity of your implementation and give a $\Theta$ bound for
its worst-case runtime. Add your answer, including your reasoning, to this
markdown file.

The worst case runtime for my implementation is $\Theta(n log n)$, the first for loop in "merge" runs $n1$ time where n1 is the length of the left subarray, and the second for loop runs $n2$ times where n2 is the length of the right subarray, the first while loop in "merge" runs in $\Theta(n1 + n2)$ time, the third while loop iterates $n1$ times, and the fourth $n2$ times which leaves the "merge" function with a time complexity of $\Theta(3n1 + 3n2)$, dropping the constants, it is $\Theta(n1 + n2)$. However this is not the expensive part of this algorithm, the first for loop in "mergesort" runs $0 to n$ times where n is the length of the input array, and the size variable doubles with each iteration, giving this for loop a $\Theta(log n)$ complexity. The second, nested for loop runs in $\Theta(n)$ time, so the total $\Theta$ complexity of this algorithm is $\Theta(n log n)$.

Help: https://www.geeksforgeeks.org/merge-sort/ I used this and the course lecture videos to get a basic understanding of how reccursive merge sort works, which I then used as a basis to implement my own iterative version.

“I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models. All of the work is my own, except where stated otherwise. I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.”