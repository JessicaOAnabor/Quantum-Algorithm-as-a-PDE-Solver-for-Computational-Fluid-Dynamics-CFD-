# Quantum-Algorithm-as-a-PDE-Solver-for-Computational-Fluid-Dynamics-CFD-

The project presents a hybrid quantum-classical algorithm designed to solve the one dimensional viscous Burgers’ equation, a nonlinear partial differential equation fundamental to modeling shockwaves and fluid dynamics phenomena. This project addresses the growing need for scalable and efficient computational fluid dynamics (CFD) solvers by exploring how near-term quantum computing can contribute to this challenge.

At the core of the approach is the use of amplitude encoding, which efficiently maps classical velocity field data into quantum states with only logarithmic qubit overhead. This encoding allows simulation of spatially discretized fields on quantum hardware with limited qubit resources, a crucial step given current hardware constraints.

To simulate the temporal evolution of the PDE, the projecr employs a hybrid variational quantum circuit that approximates one discrete time-step of the Burgers’ equation through a trotterized sequence of quantum operations, alternating Hadamard layers, parameterized Rz phase rotations, and entangling gates. This is inspired by Hamiltonian simulation and quantum tensor networks, demonstrating a fusion of quantum algorithmic concepts tailored to PDE evolution.

The quantum algorithm’s accuracy and stability are benchmarked against a classical finite-difference solver, ensuring meaningful validation. Furthermore, the project addresses the challenges posed by noisy intermediate scale quantum (NISQ) devices. It integrates noise mitigation techniques,  including Zero Noise Extrapolation (ZNE) via gate folding and measurement error correction through calibration matrices, to counteract errors arising from gate imperfections and readout noise.

Results indicate that under ideal noiseless simulation, the quantum algorithm achieves high fidelity (over 99%) with minimal divergence from classical benchmarks, confirming its correctness and robustness in principle. However, when realistic noise models are introduced, significant degradation occurs, as reflected in high Kullback-Leibler divergence and total variation distance metrics. Notably, ZNE shows limited improvement on noisy backends, suggesting that current noise mitigation strategies may be insufficient for shallow circuits under strong or symmetric noise.

Despite these limitations, the project successfully establishes a reproducible and extensible framework by leveraging deterministic seeding, comprehensive logging, and multiplatform support (including Qiskit Aer and AWS Braket). 

The impact of this projecr is multifold. It validates the feasibility of using hybrid quantum algorithms for nonlinear PDEs central to fluid dynamics, bridging classical numerical methods with emerging quantum techniques. The project also highlights the critical role of noise mitigation and provides valuable insights into the limitations of current NISQ era quantum devices for scientific computing.

Looking forward, the project opens avenues for, hopefully, advancing quantum noise correction methods, optimizing quantum circuit architectures, and scaling to more complex, higher dimensional PDEs such as the Navier-Stokes equations. Additionally, deploying these algorithms on diverse quantum hardware and integrating adaptive hybrid strategies can further unlock the potential of quantum enhanced CFD solvers.


## Dependencies

- `qiskit`
- `numpy`
- `pandas`
- `matplotlib`

## Presentation Slides

https://www.canva.com/design/DAGvtWWjZPU/ZP5dOUdidetFrkEljCVduQ/view?utm_content=DAGvtWWjZPU&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=h5af59f534d


