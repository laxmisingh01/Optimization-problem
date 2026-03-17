# Task Graph Scheduling using Genetic Algorithm

## 📌 Objective

The objective of this project is to implement task scheduling in a multiprocessor system using a Genetic Algorithm (GA). The goal is to optimally assign tasks to processors and select appropriate communication buses such that the total execution time and communication delay are minimized.

---

## 🧠 Problem Description

In a multiprocessor system, tasks are interdependent and require communication between them. Each task must be assigned to a processor, and data transfer between tasks must occur through communication buses.

The challenge lies in:

* Efficiently allocating tasks to processors
* Minimizing execution time based on processor speed (MIPS)
* Minimizing communication time based on bus transfer rates
* Respecting task dependencies (task graph)

This is a complex optimization problem (NP-hard), making Genetic Algorithm a suitable approach.

---

## 📊 Components of the System

### 1. Task Graph (DAG)

* Represents tasks and their dependencies
* Nodes represent tasks (T1, T2, etc.)
* Edges represent communication between tasks with associated data size

### 2. Processors

* Each processor has:

  * MIPS rating (Million Instructions Per Second)
  * Supported communication buses

### 3. Communication Buses

* Used for data transfer between processors
* Each bus has a specific data transfer rate

---

## 🧬 Genetic Algorithm Approach

### Chromosome Representation

Each chromosome represents a possible solution and consists of:

* Task-to-processor mapping
* Task communication-to-bus mapping

### Fitness Function

The fitness function evaluates the quality of a solution:

**Fitness = Execution Time + Communication Time**

* Execution Time = Task Size / Processor MIPS
* Communication Time = Data Size / Bus Speed (only if tasks are on different processors)

The objective is to minimize the fitness value.

---

## ⚙️ Algorithm Workflow

1. Initialize a random population of chromosomes
2. Evaluate fitness for each chromosome
3. Select the best-performing chromosomes
4. Apply crossover to generate new offspring
5. Apply mutation to introduce randomness
6. Repeat for a fixed number of generations
7. Select the best solution obtained

---

## 📈 Visualizations

The project includes the following visual outputs:

### 1. Task Graph (DAG)

* Visual representation of task dependencies

### 2. Fitness vs Generations Graph

* Shows how the solution improves over iterations
* Demonstrates convergence of the algorithm

### 3. Time Breakdown Graph

* Displays contribution of:

  * Execution Time
  * Communication Time

---

## 🧪 Results

The algorithm outputs:

* Optimal task allocation to processors
* Optimal bus assignment for communication
* Minimum total execution and communication time

Due to the stochastic nature of Genetic Algorithm, results may vary slightly on each run.

---

## 🚀 How to Run the Project

1. Open the Jupyter Notebook file
2. Run all cells sequentially
3. Observe:

   * Final optimized output
   * Graphical visualizations

algorithm minimizes total execution and communication time by intelligently assigning tasks to processors and selecting appropriate communication buses.

---

## 💡 Conclusion

The Genetic Algorithm provides an efficient way to solve complex scheduling problems where exhaustive search is not feasible. The approach is scalable and can be extended to larger systems with more tasks, processors, and communication constraints.

---

## 🔮 Future Scope

* Adding more processors and buses
* Implementing real-time scheduling constraints
* Visualizing task execution using Gantt charts
* Converting into a web-based application

---
