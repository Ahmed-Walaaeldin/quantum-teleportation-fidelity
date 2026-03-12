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

## Main Results

### 1. Ideal Teleportation Fidelity

The protocol reconstructs the input state with essentially perfect fidelity in the ideal simulator across a large set of Haar-random input states.

![Ideal teleportation fidelity](assets/teleportation_ideal_fidelity.png)

### 2. Input vs Teleported Output on the Bloch Sphere

To verify state transfer geometrically, the notebook compares Bloch-vector coordinates of selected input states against their teleported outputs.  
The overlap confirms accurate state reconstruction in the noiseless case.

![Bloch-vector comparison of input and teleported states](assets/teleportation_bloch_comparison.png)

### 3. Fidelity vs Noise Strength

The notebook studies how average teleportation fidelity changes under two realistic noise models: **depolarizing noise** and **amplitude damping**.  
This figure highlights the monotonic degradation of teleportation quality as noise strength increases.

![Teleportation fidelity versus noise strength](assets/teleportation_fidelity_vs_noise.png)

### 4. Fidelity Distributions Under Noise

Beyond average fidelity, the notebook also examines full fidelity distributions at selected depolarizing noise levels.  
This helps show how the protocol performance broadens and shifts as noise becomes stronger.

![Fidelity distributions under depolarizing noise](assets/teleportation_fidelity_distributions.png)

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
