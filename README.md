Download Link: https://assignmentchef.com/product/solved-cop4520-programming-assignment-2
<br>
<strong>Design and Implementation of Concurrent Linked List: </strong>

Design a coarse-grained locking linked list, as described in Chapter 9 of the textbook. Save this version of the linked list and call it BLOCKING_LIST. Transform your algorithm into a lockfree algorithm and call it NONBLOCKING_LIST. Your implementation should be based on Tim Harris’ paper “A Pragmatic Implementation of Non-Blocking Linked Lists.” You may also use Section 9.8 of the textbook for reference.




Evaluate your approach by executing performance comparison of your BLOCKING_LIST and NONBLOCKING_LIST. In your benchmark tests, vary the number of threads from 1 to 32 and produce graphs where you map the total execution time on the y-axis and the number of threads on the x-axis. Produce at least 3 different graphs representing different ratios of the invocation of insert, delete, and find. For example, your different ratios could be:

<ul>

 <li>Mixed: 33% insert, 33% delete, 34% find</li>

 <li>Write-dominated: 50% insert, 50% delete, 0% find</li>

 <li>Read-dominated: 15% insert, 5% delete, 80% find</li>

</ul>




To avoid “polluting” your results with the overhead of memory management (the standard malloc and free don’t scale well), you should have each thread pre-allocate its own supply of nodes, which it can keep on a private list when they are not in the list. Finally, to avoid pollution from calls to the pseudo-random (the standard rand isn’t even thread-safe), you should pregenerate enough random integers to drive the choice between insert, delete, and find for the entire test run.




Provide a brief summary of your approach and an informal statement reasoning about the correctness and efficiency of your design.




Use either C or C++ for this assignment and provide a ReadMe file with instructions explaining how to compile and run your program.