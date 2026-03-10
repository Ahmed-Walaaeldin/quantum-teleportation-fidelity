# Quantum Teleportation: Fidelity and Noise Analysis

A computational study of the standard quantum teleportation protocol using **Qiskit**.  
This project implements the full teleportation circuit, verifies correctness across **Haar-random input states**, and studies how teleportation fidelity degrades under realistic quantum noise.

## Overview

Quantum teleportation is a foundational protocol in quantum information. It allows the transfer of an unknown qubit state from one party to another using:

- a shared entangled pair,
- two classical bits of communication,
- and local correction operations.

This notebook investigates both the **ideal noiseless case** and the **noisy case**, with emphasis on fidelity and statistical robustness.

## What this project does

- Implements the standard **3-qubit teleportation circuit**
- Uses **Haar-random single-qubit states** as input
- Verifies near-unit teleportation fidelity in the ideal simulator
- Studies fidelity degradation under:
  - **Depolarizing noise**
  - **Amplitude-damping noise**
- Uses repeated experiments, convergence analysis, and statistical summaries

## Key outcomes

- Confirms that the teleportation protocol reconstructs the original state with near-perfect fidelity in the noiseless case
- Shows how fidelity decreases as noise strength increases
- Demonstrates the protocol through both theoretical explanation and numerical simulation


## Tools and libraries

- Python
- Qiskit
- Qiskit Aer
- NumPy
- Matplotlib
