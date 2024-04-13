# Multi-Threading_102117024
# Matrix Multiplication with Multi-Threading and CPU Usage Monitoring

## Overview

This Python script demonstrates how to multiply 100 matrices of size 1000x1000 using multi-threading with different numbers of threads. Additionally, it monitors and plots CPU usage for each number of threads.

## Requirements

- Python 3.x
- NumPy
- Matplotlib
- psutil

## Installation

Install the required Python packages using pip:
```bash
pip install numpy matplotlib psutil
```
## Usage

- Run the Python script `matrix_multiplication_threads_cpu_usage.py`.
- The script will generate 100 random matrices of size 1000x1000.
- It will then multiply these matrices using multi-threading with varying numbers of threads (1, 2, 3, 4, 5, 6, 7, 8).
- For each number of threads, the script measures and prints the time taken for matrix multiplication and the CPU usage.
- Finally, the script plots two graphs:
  1. Time taken vs. Number of Threads
  2. CPU Usage vs. Number of Threads

## Script Overview

- `multiply_matrices(start, end, A, B, result)`: Function to multiply a subset of matrices.
- Generate 100 random matrices (`A_matrices` and `B_matrices`) of size 1000x1000.
- Iterate over a list of thread counts (`num_threads_list`), and for each count:
  - Split the work among the specified number of threads.
  - Measure the time taken to complete the multiplication using `time.time()`.
  - Measure CPU usage using `psutil.cpu_percent(interval=1)`.
  - Plot the number of threads vs. the time taken and CPU usage using Matplotlib.

## Results

The script will output the following:

- Time taken for matrix multiplication with each number of threads.
- CPU usage percentage for each number of threads.
- Two plots:
  1. Time Taken vs. Number of Threads
  2. CPU Usage vs. Number of Threads
