# CPU Scheduling Algorithms
This project presents a collection of CPU scheduling algorithms implemented in C++. The available algorithms include First Come First Serve (FCFS), Round Robin (RR), Shortest Process Next (SPN), Shortest Remaining Time (SRT), Highest Response Ratio Next (HRRN), Feedback (FB), and Aging.


### First Come First Serve (FCFS)
- The First Come First Serve (FCFS) algorithm processes requests in the order they arrive, with no consideration for the length of the process or its priority. As a non-preemptive method, FCFS can sometimes lead to inefficiencies, especially if long processes block shorter ones.

### Round Robin with Adjustable Time Quantum (RR)
- The Round Robin (RR) scheduling technique assigns CPU time slices (or quanta) to each process in a cyclical order. This implementation allows for variable time quanta, optimizing CPU time by adjusting it according to process needs.

### Shortest Process Next (SPN)
- Shortest Process Next (SPN) prioritizes processes with the shortest burst times, executing them first. This non-preemptive algorithm aims to minimize average waiting time but can cause longer processes to wait.

### Shortest Remaining Time (SRT)
- Shortest Remaining Time (SRT) is a preemptive variant of SPN, where the currently running process can be interrupted if a new process with a shorter remaining time arrives. This algorithm dynamically adjusts priorities to optimize overall system performance.

### Highest Response Ratio Next (HRRN)
- The Highest Response Ratio Next (HRRN) algorithm selects the process with the highest response ratio, which is calculated based on waiting time and burst time. This non-preemptive method helps in balancing waiting time and service time, reducing process starvation.

### Feedback (FB)
- Feedback scheduling is a multi-level priority system that dynamically adjusts the priority of processes based on their execution history. Higher-priority processes are executed first, and upon completion, they are moved to a lower-priority queue.

### Feedback with Variable Time Quantum (FBV)
- This variant of Feedback scheduling also considers variable time quanta for each priority level, making it more adaptable to processes with varying requirements.

### Aging
- The Aging algorithm is designed to prevent process starvation by gradually increasing the priority of processes that have been waiting for an extended period. This ensures that even low-priority processes eventually receive CPU time.

## Setup Instructions

1. **Compile the Code:**
   Run the following command to compile the project:
   ```bash
   make
   ```

2. **Execute the Program:**
   After compilation, run the executable to start the simulation.

## Input Details
- **First Line:** Indicates whether to show "trace" or "stats" in output.
- **Second Line:** Specifies the scheduling algorithms to be used, along with any required parameters (e.g., time quantum for Round Robin).
- **Third Line:** The maximum simulation time.
- **Fourth Line:** The number of processes to be simulated.
- **Subsequent Lines:** Detailed descriptions of each process, including process name, arrival time, and either service time or priority, depending on the algorithm.

> **Note:** For Aging, the input format includes the process name, arrival time, and priority, instead of service time.
Example input.
stats
1
20
5
A,0,3
B,2,6
C,4,4
D,6,5
E,8,2


