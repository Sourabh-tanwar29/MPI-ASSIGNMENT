# MPI Pi Calculation

This program calculates the approximate value of π using **numerical integration** and **parallel processing** with **MPI (Message Passing Interface)**.

## Overview
The program uses the **midpoint rule** to compute the integral of the function:

\[
\int_0^1 \frac{4}{1 + x^2} \,dx
\]

This integral is equivalent to computing **π**. The work is distributed across multiple processes using **MPI**.

## How It Works
- The range `[0,1]` is divided into **num_steps** intervals.
- Each process calculates a part of the summation in parallel.
- The results are collected and summed up using `MPI_Reduce()` to get the final result.

## Prerequisites
- Install **MPI** (e.g., OpenMPI or MPICH)
- A C compiler that supports MPI (`mpicc`)

## Compilation & Execution

### Compile:
```sh
