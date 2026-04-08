# Quantum Grover Search with Error Correction and Noise Analysis

This project implements Grover’s quantum search algorithm for a 2×2 Sudoku problem and studies its behavior under noise and simple quantum error correction. It includes circuit-level implementations together with Jupyter notebook notes explaining the oracle construction, amplitude amplification, noisy dynamics, and error-corrected circuits.

The Sudoku constraints are encoded into qubits and implemented as a reversible phase oracle using ancillas and phase kickback. Grover diffusion amplifies the valid assignment. The circuit is then extended using a three-qubit repetition code to protect against bit-flip errors. A separate noise analysis studies how errors damp amplitude amplification and limit Grover performance.

## Features

- Grover circuit implementation  
- 2×2 Sudoku encoded into qubits  
- Reversible oracle construction  
- Diffusion operator implementation  
- Jupyter notebook theory notes  
- Three-qubit repetition code  
- Error-corrected Grover circuit  
- Noisy Grover simulations  

## Installation

```bash
pip install -r requirements.txt
