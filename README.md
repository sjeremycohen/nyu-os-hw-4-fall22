# nyu-os-hw-4-fall22
Part 2 (there is no part 1) - Mutex

The initial behavior is caused by NEED TO FILL THIS OUT

We see some interesting behavior with regards to time for the original vs the mutex locked version. Adding the mutex configuration adds an relatively large initial increase to the insert time. When thread count is relatively low (under 256) the mutex solution takes about 2-4x as long as the original. However this starts to taper off around 256 threads, before nearly converging somewhere around 800 threads. This is likely due to the investment in threads overtaking the investment in mutex locks, not that the mutex lock solution actually becomes faster. Our analysis is pictured below.

Based on the above, we would estimate that the true additional overhead of the mutex solution is about 3x the original solution.

It is worth noting that retrieval is completely unaltered!

![Time Comparison](./screens/part_2_time_comp.png)