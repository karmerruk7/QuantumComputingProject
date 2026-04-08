# Quantum Grover Search with Error Correction and Noise Analysis

This project implements Grover’s quantum search algorithm for a 2×2 Sudoku problem and studies its behavior under noise and simple quantum error correction. It includes circuit-level implementations together with Jupyter notebook notes explaining the oracle construction, amplitude amplification, noisy dynamics, and error-corrected circuits.

The Sudoku constraints are encoded into qubits and implemented as a reversible phase oracle using ancillas and phase kickback. Grover diffusion amplifies the valid assignment. The circuit is then extended using a three-qubit repetition code to protect against bit-flip errors. A separate noise analysis studies how errors damp amplitude amplification and limit Grover performance.

## Project Structure

- `Groverqiskit.ipynb`  
  Main Jupyter notebook containing the circuit implementation, experiments, and explanatory notes.

- `Ideal_Circuit_Design_and_a_Simple_Error_Corrected_Extension.pdf`  
  Write-up for the 2×2 Sudoku Grover circuit, including qubit encoding, reversible oracle construction, diffusion, and the three-qubit repetition-code extension.
  
- `Optimal_Runtime_of_Noisy_Amplitude_Amplification_from_Spectral_Stability.pdf`  
  Theory note on noisy Grover dynamics, spectral stability of the noisy iterate, and the resulting optimal runtime tradeoff under per-step noise.  

## Features

- **Grover circuit implementation**  
  Implements Grover’s algorithm for a 2×2 Sudoku search problem.

- **2×2 Sudoku encoded into qubits**  
  Represents the puzzle as a 4-qubit search space with a unique valid assignment. 

- **Reversible oracle construction**  
  Encodes Sudoku constraints into ancillas and applies phase kickback to mark the valid solution.  

- **Diffusion operator implementation**  
  Applies the Grover diffusion step to amplify the marked state. 

- **Jupyter notebook notes**  
  Includes notebook-based code and explanations alongside the formal PDF write-ups.

- **Three-qubit repetition code**  
  Extends the circuit with a simple bit-flip error-correcting code on the data qubits. 

- **Error-corrected Grover circuit**  
  Replaces each data qubit with an encoded logical block and inserts syndrome checks between major steps. 

- **Noisy Grover analysis**  
  Studies Grover under per-iteration CPTP noise and derives the damped-rotation picture and optimal stopping time \(T^* \asymp \min(1/\theta, 1/p)\). 

## Installation

```bash
pip install -r requirements.txt
