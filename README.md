# Quantum-Algorithm-as-a-PDE-Solver-for-Computational-Fluid-Dynamics-CFD-

# Project Goal

The primary goal is to simulate 1D viscous Burgers' equation (a nonlinear PDE modeling shockwaves) using a hybrid quantum-classical approach that leverages quantum amplitude encoding, hybrid variational circuits, and noise mitigation techniques.

## Code Overview

Main script that:

- Constructs benchmark quantum circuits (e.g., Hadamard + CNOT gates).
- Runs simulations on `AerSimulator` under:
  - Ideal (noiseless) conditions
  - Noisy conditions (depolarizing noise model)
- Measures the frequency of the all-zeros output state.
- Applies Zero-Noise Extrapolation by:
  - Duplicating (folding) noisy gates to scale noise
  - Running simulations at increasing noise levels
  - Fitting extrapolated values at zero noise
- Calculates and reports divergence metrics:
  - Kullback–Leibler (KL) divergence
  - Total Variation (TV) distance
  - L2 distance
- Outputs all results to a `.csv` summary file.

CSV file storing all simulation and ZNE results, including:

- Circuit configuration
- Raw and extrapolated measurement frequencies
- Ideal probabilities
- Error bars and confidence intervals
- Divergence metrics

---

## Dependencies

- `qiskit`
- `numpy`
- `pandas`
- `matplotlib`

