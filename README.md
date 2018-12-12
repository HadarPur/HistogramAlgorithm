# HistogramAlgorithm
Calculating the histogram of the very large array of integers using MPI + OpenMP + CUDA environment.

## Requirements:

•	Run two processes

•	The given array A is known to one of these processes, say process 0

•	The range of values of members in array A is [0, 255]. The number of members of A is 200000. You may initiate the array A randomly

•	Process 0 sends half of the array A to process 1 

•	Both processes work on their parts of A concurrently, using OpenMP for the first portion of their part and CUDA for the second. Each of CUDA threads manage at most 500 numbers of original array.

•	Process 1 sends the results of CUDA and OpenMP of its part to process 0

•	Process 0 combines its results with the results of process 1 with OpenMP

•	Process 0 displays the final histogram of the initial array A
