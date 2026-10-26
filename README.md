# awesome-quantum

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[日本語版はこちら / Japanese](README.ja.md)

Curated quantum computing resources — SDKs, simulators, error correction, optimization and annealing, applications, HPC integration, post-quantum cryptography, cloud services and learning material, with an engineering (CAE/HPC) angle. ⭐ badges show live GitHub star counts (via shields.io); release badges show the date of the latest GitHub release (YYYY/MM/DD, as of the last refresh); last-commit badges show live commit activity (via shields.io).

## Index

- [SDKs & programming frameworks](#sdks--programming-frameworks)
- [Simulators & tensor networks](#simulators--tensor-networks)
- [Error correction, mitigation & fault tolerance](#error-correction-mitigation--fault-tolerance)
- [Optimization & quantum annealing](#optimization--quantum-annealing)
- [Chemistry, materials & machine learning](#chemistry-materials--machine-learning)
- [Quantum for engineering, CAE & HPC](#quantum-for-engineering-cae--hpc)
- [Post-quantum cryptography](#post-quantum-cryptography)
- [Cloud quantum services](#cloud-quantum-services)
- [Learning resources](#learning-resources)
- [Japanese learning resources](#japanese-learning-resources)
- [Related lists](#related-lists)
- [shvyac's awesome lists](#shvyacs-awesome-lists)

---

## SDKs & programming frameworks

General-purpose toolkits for building, transpiling and running quantum circuits on simulators and real hardware.

### Qiskit
IBM-led open-source SDK (Python/Rust/C) for circuits, operators and primitives; the most widely used quantum SDK. IBM Quantum hardware is accessed via qiskit-ibm-runtime.

- https://www.ibm.com/quantum/qiskit
- https://github.com/Qiskit/qiskit ![GitHub stars](https://img.shields.io/github/stars/Qiskit/qiskit?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F22-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Qiskit/qiskit?style=flat)
- https://github.com/Qiskit/qiskit-ibm-runtime ![GitHub stars](https://img.shields.io/github/stars/Qiskit/qiskit-ibm-runtime?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F22-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Qiskit/qiskit-ibm-runtime?style=flat)

### Cirq
Google Quantum AI's Python framework for NISQ circuits, with fine-grained control over gates, moments and device constraints.

- https://quantumai.google/cirq
- https://github.com/quantumlib/Cirq ![GitHub stars](https://img.shields.io/github/stars/quantumlib/Cirq?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F06%2F30-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/quantumlib/Cirq?style=flat)

### PennyLane / Catalyst
Xanadu's differentiable quantum programming platform (QML, chemistry, optimization) with JAX/PyTorch integration; Catalyst adds JIT compilation of hybrid programs (MLIR/QIR).

- https://pennylane.ai/
- https://github.com/PennyLaneAI/pennylane ![GitHub stars](https://img.shields.io/github/stars/PennyLaneAI/pennylane?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F06%2F26-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/PennyLaneAI/pennylane?style=flat)
- https://github.com/PennyLaneAI/catalyst ![GitHub stars](https://img.shields.io/github/stars/PennyLaneAI/catalyst?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F05%2F12-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/PennyLaneAI/catalyst?style=flat)

### CUDA-Q
NVIDIA's C++/Python programming model for hybrid quantum-classical workflows, running on GPU simulators, multi-GPU clusters and many QPU backends.

- https://developer.nvidia.com/cuda-q
- https://github.com/NVIDIA/cuda-quantum ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/cuda-quantum?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F12-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/NVIDIA/cuda-quantum?style=flat)

### Microsoft Quantum Development Kit (QDK)
Q# language, resource estimator, OpenQASM support and Quantum Katas tutorials in one repository (successor of the archived microsoft/Quantum samples).

- https://learn.microsoft.com/azure/quantum/
- https://github.com/microsoft/qdk ![GitHub stars](https://img.shields.io/github/stars/microsoft/qdk?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F06-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/microsoft/qdk?style=flat)

### Amazon Braket SDK
Python SDK for Amazon Braket — run circuits and analog Hamiltonian simulations on multiple vendors' QPUs and managed simulators.

- https://github.com/amazon-braket/amazon-braket-sdk-python ![GitHub stars](https://img.shields.io/github/stars/amazon-braket/amazon-braket-sdk-python?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F23-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/amazon-braket/amazon-braket-sdk-python?style=flat)

### TKET
Quantinuum's retargetable quantum compiler (C++ core, pytket Python API) with circuit optimisation passes and many hardware backends.

- https://docs.quantinuum.com/tket/
- https://github.com/Quantinuum/tket ![GitHub stars](https://img.shields.io/github/stars/Quantinuum/tket?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F08-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Quantinuum/tket?style=flat)

### pyQuil / Yao.jl / Tequila / qBraid
Rigetti's Quil-based Python library (pyQuil); extensible Julia framework for quantum algorithm design (Yao.jl); high-level abstraction for variational algorithms (Tequila); platform-agnostic runtime and transpiler between SDKs (qBraid).

- https://github.com/rigetti/pyquil ![GitHub stars](https://img.shields.io/github/stars/rigetti/pyquil?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F08-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/rigetti/pyquil?style=flat)
- https://github.com/QuantumBFS/Yao.jl ![GitHub stars](https://img.shields.io/github/stars/QuantumBFS/Yao.jl?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F03%2F01-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/QuantumBFS/Yao.jl?style=flat)
- https://github.com/tequilahub/tequila ![GitHub stars](https://img.shields.io/github/stars/tequilahub/tequila?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F05-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/tequilahub/tequila?style=flat)
- https://github.com/qBraid/qBraid ![GitHub stars](https://img.shields.io/github/stars/qBraid/qBraid?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F02-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/qBraid/qBraid?style=flat)

---

## Simulators & tensor networks

Classical simulation of quantum circuits and many-body systems — state-vector, density-matrix, stabilizer and tensor-network methods, many GPU/HPC-accelerated.

### Qiskit Aer
High-performance circuit simulator with realistic noise models, GPU and MPI support.

- https://github.com/Qiskit/qiskit-aer ![GitHub stars](https://img.shields.io/github/stars/Qiskit/qiskit-aer?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F20-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Qiskit/qiskit-aer?style=flat)

### NVIDIA cuQuantum
GPU libraries for state-vector (cuStateVec), tensor-network (cuTensorNet) and density-matrix simulation; used as a backend by Qiskit Aer, Cirq/qsim, PennyLane and CUDA-Q.

- https://developer.nvidia.com/cuquantum-sdk
- https://github.com/NVIDIA/cuQuantum ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/cuQuantum?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F10-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/NVIDIA/cuQuantum?style=flat)

### Qulacs
Fast C++/Python variational circuit simulator developed in Japan (Osaka University / QunaSys origin).

- https://github.com/qulacs/qulacs ![GitHub stars](https://img.shields.io/github/stars/qulacs/qulacs?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F29-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/qulacs/qulacs?style=flat)

### qsim / QuEST
Google's optimized state-vector simulator integrated with Cirq (qsim); multithreaded, distributed and GPU-accelerated simulator from Oxford (QuEST).

- https://github.com/quantumlib/qsim ![GitHub stars](https://img.shields.io/github/stars/quantumlib/qsim?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F06%2F24-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/quantumlib/qsim?style=flat)
- https://github.com/QuEST-Kit/QuEST ![GitHub stars](https://img.shields.io/github/stars/QuEST-Kit/QuEST?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F24-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/QuEST-Kit/QuEST?style=flat)

### QuTiP
Quantum Toolbox in Python — open quantum systems, master equations, quantum optics and pulse-level dynamics.

- https://qutip.org/
- https://github.com/qutip/qutip ![GitHub stars](https://img.shields.io/github/stars/qutip/qutip?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F04-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/qutip/qutip?style=flat)

### quimb / ITensors.jl
Tensor-network libraries for quantum information, circuit simulation and many-body physics (DMRG, MPS, PEPS) in Python (quimb) and Julia (ITensors.jl).

- https://github.com/jcmgray/quimb ![GitHub stars](https://img.shields.io/github/stars/jcmgray/quimb?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F10-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/jcmgray/quimb?style=flat)
- https://github.com/ITensor/ITensors.jl ![GitHub stars](https://img.shields.io/github/stars/ITensor/ITensors.jl?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F27-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/ITensor/ITensors.jl?style=flat)

---

## Error correction, mitigation & fault tolerance

Tools for quantum error correction (QEC) research, error mitigation on today's noisy hardware, and resource estimation for fault-tolerant algorithms.

### Stim / PyMatching
Very fast stabilizer-circuit simulator and sampler for QEC experiments (Stim); minimum-weight perfect matching decoder for surface codes and other QEC codes (PyMatching).

- https://github.com/quantumlib/Stim ![GitHub stars](https://img.shields.io/github/stars/quantumlib/Stim?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F05%2F22-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/quantumlib/Stim?style=flat)
- https://github.com/oscarhiggott/PyMatching ![GitHub stars](https://img.shields.io/github/stars/oscarhiggott/PyMatching?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F09%2F25-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/oscarhiggott/PyMatching?style=flat)

### Mitiq
Unitary Foundation's toolkit for error mitigation (zero-noise extrapolation, probabilistic error cancellation, etc.) across most quantum SDKs and hardware.

- https://mitiq.readthedocs.io/
- https://github.com/unitaryfoundation/mitiq ![GitHub stars](https://img.shields.io/github/stars/unitaryfoundation/mitiq?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F04-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/unitaryfoundation/mitiq?style=flat)

### Qualtran
Google's library for expressing and analysing fault-tolerant quantum algorithms, including qubit and T-gate resource estimation.

- https://github.com/quantumlib/Qualtran ![GitHub stars](https://img.shields.io/github/stars/quantumlib/Qualtran?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F01%2F22-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/quantumlib/Qualtran?style=flat)

---

## Optimization & quantum annealing

QUBO / Ising formulations, quantum annealers and quantum-inspired solvers for combinatorial optimization (scheduling, routing, design optimization).

### D-Wave Ocean SDK
Python tools for formulating problems (BQM/CQM, dimod) and solving them on D-Wave quantum annealers, hybrid solvers or classical samplers.

- https://docs.dwavequantum.com/
- https://github.com/dwavesystems/dwave-ocean-sdk ![GitHub stars](https://img.shields.io/github/stars/dwavesystems/dwave-ocean-sdk?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F15-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/dwavesystems/dwave-ocean-sdk?style=flat)

### OpenJij / PyQUBO
Japanese open-source Ising/QUBO framework with simulated and simulated-quantum annealing (OpenJij, by Jij); DSL for building QUBOs from mathematical expressions (PyQUBO, by Recruit).

- https://github.com/Jij-Inc/OpenJij ![GitHub stars](https://img.shields.io/github/stars/Jij-Inc/OpenJij?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Jij-Inc/OpenJij?style=flat)
- https://github.com/recruit-communications/pyqubo ![GitHub stars](https://img.shields.io/github/stars/recruit-communications/pyqubo?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2022%2F12%2F13-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/recruit-communications/pyqubo?style=flat)

### Simulated Bifurcation
CPU/GPU (PyTorch) implementation of the Simulated Bifurcation algorithm — a quantum-inspired Ising/QUBO solver originally proposed by Toshiba.

- https://github.com/bqth29/simulated-bifurcation-algorithm ![GitHub stars](https://img.shields.io/github/stars/bqth29/simulated-bifurcation-algorithm?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F04%2F10-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/bqth29/simulated-bifurcation-algorithm?style=flat)

---

## Chemistry, materials & machine learning

Application libraries for electronic-structure problems, quantum machine learning and sample-based methods.

### OpenFermion / Qiskit Nature
Compile and analyse quantum algorithms for electronic structure and fermionic systems (OpenFermion); Qiskit framework for chemistry, physics and other natural-science problems (Qiskit Nature).

- https://github.com/quantumlib/OpenFermion ![GitHub stars](https://img.shields.io/github/stars/quantumlib/OpenFermion?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F17-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/quantumlib/OpenFermion?style=flat)
- https://github.com/qiskit-community/qiskit-nature ![GitHub stars](https://img.shields.io/github/stars/qiskit-community/qiskit-nature?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F06%2F01-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/qiskit-community/qiskit-nature?style=flat)

### Qiskit SQD addon
Sample-based Quantum Diagonalization — classically post-processes noisy quantum samples (often on HPC) to estimate eigenvalues for chemistry problems.

- https://github.com/Qiskit/qiskit-addon-sqd ![GitHub stars](https://img.shields.io/github/stars/Qiskit/qiskit-addon-sqd?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F08-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/Qiskit/qiskit-addon-sqd?style=flat)

### Qiskit Machine Learning
Quantum kernels, quantum neural networks and PyTorch integration for QML experiments on simulators and hardware.

- https://github.com/qiskit-community/qiskit-machine-learning ![GitHub stars](https://img.shields.io/github/stars/qiskit-community/qiskit-machine-learning?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F19-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/qiskit-community/qiskit-machine-learning?style=flat)

---

## Quantum for engineering, CAE & HPC

Integrating quantum processors with HPC centres and exploring quantum algorithms for engineering simulation (CFD, PDEs).

### QRMI / Slurm SPANK plugins
Vendor-agnostic Quantum Resource Management Interface for on-prem or cloud QPUs (QRMI, Rust/Python/C) and Slurm plugins to schedule quantum resources as part of HPC jobs.

- https://github.com/qiskit-community/qrmi ![GitHub stars](https://img.shields.io/github/stars/qiskit-community/qrmi?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F23-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/qiskit-community/qrmi?style=flat)
- https://github.com/qiskit-community/spank-plugins ![GitHub stars](https://img.shields.io/github/stars/qiskit-community/spank-plugins?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F21-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/qiskit-community/spank-plugins?style=flat)

### OQTOPUS
Open Quantum Toolchain for OPerators & USers — open-source software architecture for operating cloud quantum computers, developed in Japan (Osaka University and partners).

- https://github.com/oqtopus-team/oqtopus-cloud ![GitHub stars](https://img.shields.io/github/stars/oqtopus-team/oqtopus-cloud?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F11-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/oqtopus-team/oqtopus-cloud?style=flat)

### Quantum CFD research
EU Horizon project QCFD (quantum algorithms for computational fluid dynamics) and TUHH's research page on quantum CFD.

- https://cordis.europa.eu/project/id/101080085 — EU CORDIS: QCFD project
- https://www.tuhh.de/fds/research/current/qcfd — TUHH QCFD

---

## Post-quantum cryptography

Preparing classical systems for quantum-capable adversaries.

### liboqs (Open Quantum Safe)
C library of quantum-resistant KEMs and signatures (including the NIST ML-KEM / ML-DSA standards) for prototyping and integration into TLS/SSH.

- https://openquantumsafe.org/
- https://github.com/open-quantum-safe/liboqs ![GitHub stars](https://img.shields.io/github/stars/open-quantum-safe/liboqs?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F09-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/open-quantum-safe/liboqs?style=flat)

### NIST PQC
NIST's post-quantum cryptography standardization project (FIPS 203/204/205).

- https://csrc.nist.gov/projects/post-quantum-cryptography

---

## Cloud quantum services

Managed access to real quantum hardware.

### Cloud platforms
Major cloud entry points for running jobs on QPUs.

- https://quantum.cloud.ibm.com/ — IBM Quantum Platform
- https://aws.amazon.com/braket/ — Amazon Braket (multi-vendor QPUs)
- https://azure.microsoft.com/solutions/quantum-computing — Azure Quantum
- https://quantumai.google/ — Google Quantum AI
- https://www.dwavequantum.com/solutions-and-products/cloud-platform/ — D-Wave Leap (annealing & hybrid solvers)

---

## Learning resources

Courses, textbooks and interactive tutorials.

### Courses & tutorials
Free, official learning paths.

- https://quantum.cloud.ibm.com/learning — IBM Quantum Learning (Qiskit courses)
- https://pennylane.ai/codebook — PennyLane Codebook
- https://github.com/microsoft/qdk/tree/main/katas — Microsoft Quantum Katas (in the QDK repository)
- https://quantum.country/ — Quantum Country (spaced-repetition essays by Matuschak & Nielsen)
- https://qosf.org/ — Quantum Open Source Foundation (mentorship, project lists)

---

## Japanese learning resources

Free Japanese-language quantum materials for students at Japanese universities and colleges (日本語の教材).

### Quantum Academy of Science and Technology (量子技術高等教育拠点)
University-level hub run by NII with the University of Tokyo, Nagoya, Kyushu and Keio universities — online lectures, an open materials database (CC BY-SA) and a standard curriculum, undergraduate to graduate level (Q-LEAP program).

- https://qacademy.jp/
- https://www.nii.ac.jp/news/upload/nii_newsrelease_20230612.pdf — NII press release on the open materials database

### UTokyo Quantum Education for Future Technologies (QEd)
University of Tokyo lecture series with videos and slides on quantum hardware platforms: photonic quantum computing and communication, trapped ions, optical lattice clocks, cold-atom quantum simulation, electrons on helium and NMR.

- https://ch.u-tokyo.ac.jp/series/?id=DAPjNC3oaALB — UTokyo Channel
- https://ocw.u-tokyo.ac.jp/lecture_files/11447/1/notes/ja/QEd_introduction.pdf — introduction slides

### Quantum Native Dojo
QunaSys's free self-study course from quantum-computing basics to NISQ algorithms and error correction, as Jupyter notebooks runnable on Google Colab (undergraduate math background). Also published as a book by Kodansha.

- https://dojo.qulacs.org/ja/latest/
- https://github.com/qulacs/quantum-native-dojo ![GitHub stars](https://img.shields.io/github/stars/qulacs/quantum-native-dojo?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/qulacs/quantum-native-dojo?style=flat)

### Quantum Tokyo
Japanese Qiskit community — Japanese translations of IBM Quantum Learning courses (e.g. Basics of Quantum Information), Qiskit getting-started guides and Qiskit Global Summer School materials.

- https://quantum-tokyo.github.io/introduction/intro.html
- https://github.com/quantum-tokyo/introduction ![GitHub stars](https://img.shields.io/github/stars/quantum-tokyo/introduction?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/quantum-tokyo/introduction?style=flat)

### Annealing & optimization tutorials
Japanese tutorials on Ising models, QUBO/HUBO, combinatorial optimization and quantum annealing.

- https://tutorial.openjij.org/ja/intro.html — OpenJij Book (Jij)
- https://amplify.fixstars.com/ja/demo — Fixstars Amplify online demos & tutorials (free registration)

### Quantum mechanics foundations
Background physics in Japanese.

- https://eman-physics.net/quantum/contents.html — EMAN's Quantum Mechanics (undergraduate physics, personal site)
- https://ocw.kyoto-u.ac.jp/ — Kyoto University OCW (lecture videos and notes, CC BY-NC-SA)

---

## Related lists

- https://github.com/desireevl/awesome-quantum-computing ![GitHub stars](https://img.shields.io/github/stars/desireevl/awesome-quantum-computing?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/desireevl/awesome-quantum-computing?style=flat) — quantum computing learning & developing resources
- https://github.com/qosf/awesome-quantum-software ![GitHub stars](https://img.shields.io/github/stars/qosf/awesome-quantum-software?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/qosf/awesome-quantum-software?style=flat) — open-source quantum software projects
- https://github.com/krishnakumarsekar/awesome-quantum-machine-learning ![GitHub stars](https://img.shields.io/github/stars/krishnakumarsekar/awesome-quantum-machine-learning?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/krishnakumarsekar/awesome-quantum-machine-learning?style=flat) — quantum machine learning basics, algorithms and materials
- https://github.com/artix41/awesome-quantum-ml ![GitHub stars](https://img.shields.io/github/stars/artix41/awesome-quantum-ml?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/artix41/awesome-quantum-ml?style=flat) — quantum machine learning papers
- https://github.com/veorq/awesome-post-quantum ![GitHub stars](https://img.shields.io/github/stars/veorq/awesome-post-quantum?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/veorq/awesome-post-quantum?style=flat) — post-quantum cryptography
- https://github.com/francois-marie/awesome-quantum-computing-experiments ![GitHub stars](https://img.shields.io/github/stars/francois-marie/awesome-quantum-computing-experiments?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F07%2F15-blue?style=flat) ![Last commit](https://img.shields.io/github/last-commit/francois-marie/awesome-quantum-computing-experiments?style=flat) — database of notable quantum experiments (QEC focus)
- https://github.com/poig/Qc_book_list ![GitHub stars](https://img.shields.io/github/stars/poig/Qc_book_list?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/poig/Qc_book_list?style=flat) — books for self-studying quantum computing
- https://github.com/shvyac/awesome-hpc ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hpc?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/shvyac/awesome-hpc?style=flat) — HPC tools (schedulers, MPI, GPU)
- https://github.com/shvyac/awesome-open-source-solvers ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-open-source-solvers?style=flat&label=%E2%AD%90) ![Last commit](https://img.shields.io/github/last-commit/shvyac/awesome-open-source-solvers?style=flat) — open-source FEM/CFD/scientific solvers
- https://awesome.re/ — Awesome manifesto

---

## shvyac's awesome lists

All curated lists maintained by [shvyac](https://github.com/shvyac):

- [awesome-AI-Powered-Executive-Dashboards](https://github.com/shvyac/awesome-AI-Powered-Executive-Dashboards) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-AI-Powered-Executive-Dashboards?style=flat&label=%E2%AD%90)
- [awesome-ai-tool-for-mechanical-engineering](https://github.com/shvyac/awesome-ai-tool-for-mechanical-engineering) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ai-tool-for-mechanical-engineering?style=flat&label=%E2%AD%90)
- [awesome-audio-softwares](https://github.com/shvyac/awesome-audio-softwares) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-audio-softwares?style=flat&label=%E2%AD%90)
- [awesome-azure-ai-dynamics365-security](https://github.com/shvyac/awesome-azure-ai-dynamics365-security) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-azure-ai-dynamics365-security?style=flat&label=%E2%AD%90)
- [awesome-ballroom-dance](https://github.com/shvyac/awesome-ballroom-dance) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ballroom-dance?style=flat&label=%E2%AD%90)
- [awesome-cad-cae](https://github.com/shvyac/awesome-cad-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cad-cae?style=flat&label=%E2%AD%90)
- [awesome-cms-ai](https://github.com/shvyac/awesome-cms-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-cms-ai?style=flat&label=%E2%AD%90)
- [awesome-dashboards-visualization](https://github.com/shvyac/awesome-dashboards-visualization) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-dashboards-visualization?style=flat&label=%E2%AD%90)
- [awesome-ghost-artists](https://github.com/shvyac/awesome-ghost-artists) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-ghost-artists?style=flat&label=%E2%AD%90)
- [awesome-hamradio](https://github.com/shvyac/awesome-hamradio) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hamradio?style=flat&label=%E2%AD%90)
- [awesome-hpc](https://github.com/shvyac/awesome-hpc) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hpc?style=flat&label=%E2%AD%90)
- [awesome-iso27001-isms-tools](https://github.com/shvyac/awesome-iso27001-isms-tools) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-iso27001-isms-tools?style=flat&label=%E2%AD%90)
- [awesome-local-llm](https://github.com/shvyac/awesome-local-llm) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-local-llm?style=flat&label=%E2%AD%90)
- [awesome-m5stack-arduino](https://github.com/shvyac/awesome-m5stack-arduino) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-m5stack-arduino?style=flat&label=%E2%AD%90)
- [awesome-map-gis](https://github.com/shvyac/awesome-map-gis) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-map-gis?style=flat&label=%E2%AD%90)
- [awesome-meshless-cae](https://github.com/shvyac/awesome-meshless-cae) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-meshless-cae?style=flat&label=%E2%AD%90)
- [awesome-online-services](https://github.com/shvyac/awesome-online-services) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-online-services?style=flat&label=%E2%AD%90)
- [awesome-open-source-solvers](https://github.com/shvyac/awesome-open-source-solvers) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-open-source-solvers?style=flat&label=%E2%AD%90)
- [awesome-osint-ai](https://github.com/shvyac/awesome-osint-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-osint-ai?style=flat&label=%E2%AD%90)
- [awesome-quantum](https://github.com/shvyac/awesome-quantum) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-quantum?style=flat&label=%E2%AD%90)
- [awesome-redmine-ai](https://github.com/shvyac/awesome-redmine-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-redmine-ai?style=flat&label=%E2%AD%90)
- [awesome-requirements-system-ai](https://github.com/shvyac/awesome-requirements-system-ai) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-requirements-system-ai?style=flat&label=%E2%AD%90)
- [awesome-trading-stock](https://github.com/shvyac/awesome-trading-stock) ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-trading-stock?style=flat&label=%E2%AD%90)
