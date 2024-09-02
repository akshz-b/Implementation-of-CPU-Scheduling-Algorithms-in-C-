# CPU Scheduling Algorithms

This project showcases various CPU scheduling algorithms implemented in C++. The algorithms available include First Come First Serve (FCFS), Round Robin (RR), Shortest Process Next (SPN), Shortest Remaining Time (SRT), Highest Response Ratio Next (HRRN), Feedback (FB), and Aging.

## Algorithms

### First Come First Serve (FCFS)
- FCFS processes tasks in the order they arrive without considering their length or priority. This non-preemptive approach can sometimes lead to inefficiencies if long processes block shorter ones.

### Round Robin with Adjustable Time Quantum (RR)
- Round Robin (RR) assigns CPU time slices to processes in a cyclic order. This implementation features variable time quanta, allowing the time slice to be adjusted according to each process's needs, optimizing CPU time allocation.

### Shortest Process Next (SPN)
- SPN prioritizes processes with the shortest burst times, executing them first. As a non-preemptive algorithm, it focuses on minimizing average waiting time but can result in longer processes being delayed.

### Shortest Remaining Time (SRT)
- SRT is a preemptive version of SPN, allowing the current process to be interrupted if a new process with a shorter remaining time arrives. This dynamic adjustment aims to improve overall system performance.

### Highest Response Ratio Next (HRRN)
- HRRN selects the process with the highest response ratio, calculated based on waiting time and burst time. This non-preemptive method helps balance waiting time and service time, reducing the risk of process starvation.

### Feedback (FB)
- Feedback scheduling utilizes a multi-level priority system, dynamically adjusting process priorities based on their execution history. Higher-priority processes are executed first, and once they complete, they are moved to a lower-priority queue.

### Aging
- The Aging algorithm prevents process starvation by gradually increasing the priority of processes that have waited for an extended period, ensuring even low-priority processes receive CPU time.

## Setup Instructions

1. **Compile the Code:**
   To compile the project, use the following commands:
   ```bash
   g++ -c main.cpp
   g++ -o schedular main.o
   ```

2. **Execute the Program:**
   After compiling, run the executable named `schedular` to start the simulation.

## Input Format

- **First Line:** Specify "trace" or "stats" to determine the output format.
- **Second Line:** List the CPU scheduling algorithms to be used, along with any parameters like time quantum for Round Robin.
- **Third Line:** Specify the maximum time for the simulation.
- **Fourth Line:** Indicate the number of processes to be simulated.
- **Subsequent Lines:** Provide a description of each process, including its name, arrival time, and either service time or priority (depending on the algorithm).

### Example Input
```
trace
1
21
5
A,0,5
B,2,4
C,1,1
D,6,4
E,8,7
```

