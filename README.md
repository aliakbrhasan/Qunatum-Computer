# 🧠 Quantum VQE Simulation for 1D Heisenberg Chain

This project implements a **Variational Quantum Eigensolver (VQE)** algorithm using Qiskit to compute the **ground state energy per spin** for a 1D Heisenberg spin chain. The code supports execution on both **quantum simulators** (e.g., AerSimulator) and **real IBM quantum hardware**.

## 📌 Features

- Models a 1D Heisenberg Hamiltonian using Qiskit Nature.
- Calculates the ground state energy per spin using:
  - **Qiskit Aer Simulator**
  - **IBM Quantum Backends**
- Compares results with classical exact solutions (NumPy Eigensolver).
- Modular and scalable code supporting variable lattice sizes and boundary conditions.
- Includes visualization of the lattice and energy convergence.

## 🛠 Requirements

This notebook requires the following Python libraries:

```bash
qiskit
qiskit-aer
qiskit-nature
qiskit-ibm-runtime
qiskit-algorithms
rustworkx
numpy
```

Install all dependencies with:

```bash
pip install qiskit qiskit-aer qiskit-nature qiskit-ibm-runtime qiskit-algorithms rustworkx numpy
```

You also need an IBM Quantum account. Authenticate using:

```python
from qiskit_ibm_runtime import QiskitRuntimeService
QiskitRuntimeService.save_account("<YOUR_IBM_TOKEN>", overwrite=True)
```

## 📂 File Overview

- `Final_Code_Spin.ipynb` — Main notebook with VQE implementation, simulation, hardware execution, and results comparison.
- `README.md` — This documentation file.

## ▶️ How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/quantum-vqe-heisenberg.git
   cd quantum-vqe-heisenberg
   ```

2. Open the notebook:
   ```bash
   jupyter notebook Final_Code_Spin.ipynb
   ```

3. Select simulation or hardware backend inside the notebook and run all cells.

## 📊 Output

- Ground state energy estimates for different spin chains
- Circuit depth and transpilation reports

## 🧪 Physics Model

The code simulates the **Heisenberg Hamiltonian** for a 1D spin chain:

\[
H = \sum_{i} J_x S^x_i S^x_{i+1} + J_y S^y_i S^y_{i+1} + J_z S^z_i S^z_{i+1}
\]

The model is implemented using Qiskit Nature's `HeisenbergModel` and solved using the `VQE` algorithm with various ansatz circuits such as `EfficientSU2` and `RealAmplitudes`.

## 🤖 Backend Options

- `AerSimulator` (default)
- Real quantum devices like `ibmq_qasm_simulator`, `ibmq_jakarta`, etc.

## 🧠 Author

Ali Akbr Hasan Ali
Laboratory Assistant – Department of Physics, University of Kerbala  
personal Email: aliakbr.h.a@gmail.com

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).

## ⭐ Acknowledgments

- IBM Quantum and Qiskit teams
- Qiskit Nature development community

