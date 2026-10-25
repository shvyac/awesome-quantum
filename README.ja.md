# awesome-quantum（日本語）

[English README](README.md)

量子コンピューティングのリソース集。SDK、シミュレータ、誤り訂正、最適化・量子アニーリング、応用、HPC 連携、耐量子暗号、クラウドサービス、学習教材を、エンジニアリング(CAE/HPC)の視点も交えて整理。⭐ バッジは GitHub のスター数をリアルタイム表示します(shields.io)。release バッジは GitHub の最新リリース日(YYYY/MM/DD、最終更新時点)を示します。

## 目次

- [SDK・プログラミングフレームワーク](#sdkプログラミングフレームワーク)
- [シミュレータとテンソルネットワーク](#シミュレータとテンソルネットワーク)
- [誤り訂正・エラー緩和・誤り耐性](#誤り訂正エラー緩和誤り耐性)
- [最適化と量子アニーリング](#最適化と量子アニーリング)
- [化学・材料・機械学習](#化学材料機械学習)
- [エンジニアリング・CAE・HPC と量子](#エンジニアリングcaehpc-と量子)
- [耐量子暗号](#耐量子暗号)
- [クラウド量子サービス](#クラウド量子サービス)
- [学習リソース](#学習リソース)
- [関連リスト](#関連リスト)
- [shvyac の awesome リスト](#shvyac-の-awesome-リスト)

---

## SDK・プログラミングフレームワーク

量子回路を作成・変換し、シミュレータや実機で実行するための汎用ツールキット。

### Qiskit
IBM 主導のオープンソース SDK(Python/Rust/C)。回路・演算子・プリミティブを扱う、最も広く使われている量子 SDK。IBM Quantum の実機には qiskit-ibm-runtime 経由で接続。

- https://www.ibm.com/quantum/qiskit
- https://github.com/Qiskit/qiskit ![GitHub stars](https://img.shields.io/github/stars/Qiskit/qiskit?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F22-blue?style=flat)
- https://github.com/Qiskit/qiskit-ibm-runtime ![GitHub stars](https://img.shields.io/github/stars/Qiskit/qiskit-ibm-runtime?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F22-blue?style=flat)

### Cirq
Google Quantum AI による NISQ 回路向け Python フレームワーク。ゲート・モーメント・デバイス制約を細かく制御できる。

- https://quantumai.google/cirq
- https://github.com/quantumlib/Cirq ![GitHub stars](https://img.shields.io/github/stars/quantumlib/Cirq?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F06%2F30-blue?style=flat)

### PennyLane / Catalyst
Xanadu による微分可能な量子プログラミング基盤(量子機械学習・量子化学・最適化)。JAX/PyTorch と連携。Catalyst はハイブリッドプログラムを JIT コンパイル(MLIR/QIR)。

- https://pennylane.ai/
- https://github.com/PennyLaneAI/pennylane ![GitHub stars](https://img.shields.io/github/stars/PennyLaneAI/pennylane?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F06%2F26-blue?style=flat)
- https://github.com/PennyLaneAI/catalyst ![GitHub stars](https://img.shields.io/github/stars/PennyLaneAI/catalyst?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F05%2F12-blue?style=flat)

### CUDA-Q
NVIDIA の量子・古典ハイブリッド向け C++/Python プログラミングモデル。GPU シミュレータ・マルチ GPU クラスタ・多数の QPU バックエンドで実行。

- https://developer.nvidia.com/cuda-q
- https://github.com/NVIDIA/cuda-quantum ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/cuda-quantum?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F12-blue?style=flat)

### Microsoft Quantum Development Kit (QDK)
Q# 言語・リソース見積もり・OpenQASM 対応・Quantum Katas チュートリアルを1つにまとめたリポジトリ(アーカイブ済みの microsoft/Quantum サンプルの後継)。

- https://learn.microsoft.com/azure/quantum/
- https://github.com/microsoft/qdk ![GitHub stars](https://img.shields.io/github/stars/microsoft/qdk?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F06-blue?style=flat)

### Amazon Braket SDK
Amazon Braket 用 Python SDK。複数ベンダーの QPU やマネージドシミュレータで回路・アナログハミルトニアンシミュレーションを実行。

- https://github.com/amazon-braket/amazon-braket-sdk-python ![GitHub stars](https://img.shields.io/github/stars/amazon-braket/amazon-braket-sdk-python?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F23-blue?style=flat)

### TKET
Quantinuum のハードウェア非依存な量子コンパイラ(C++ コア、Python API の pytket)。回路最適化パスと多数のバックエンドを提供。

- https://docs.quantinuum.com/tket/
- https://github.com/Quantinuum/tket ![GitHub stars](https://img.shields.io/github/stars/Quantinuum/tket?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F08-blue?style=flat)

### pyQuil / Yao.jl / Tequila / qBraid
Rigetti の Quil ベース Python ライブラリ(pyQuil)；Julia 製の拡張性の高い量子アルゴリズム設計フレームワーク(Yao.jl)；変分アルゴリズム向けの高水準抽象化(Tequila)；SDK 間のトランスパイルを行うプラットフォーム非依存ランタイム(qBraid)。

- https://github.com/rigetti/pyquil ![GitHub stars](https://img.shields.io/github/stars/rigetti/pyquil?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F08-blue?style=flat)
- https://github.com/QuantumBFS/Yao.jl ![GitHub stars](https://img.shields.io/github/stars/QuantumBFS/Yao.jl?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F03%2F01-blue?style=flat)
- https://github.com/tequilahub/tequila ![GitHub stars](https://img.shields.io/github/stars/tequilahub/tequila?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F05-blue?style=flat)
- https://github.com/qBraid/qBraid ![GitHub stars](https://img.shields.io/github/stars/qBraid/qBraid?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F02-blue?style=flat)

---

## シミュレータとテンソルネットワーク

量子回路・多体系の古典シミュレーション。状態ベクトル・密度行列・スタビライザ・テンソルネットワーク法など(GPU/HPC 対応のものが多い)。

### Qiskit Aer
現実的なノイズモデル、GPU・MPI に対応した高性能回路シミュレータ。

- https://github.com/Qiskit/qiskit-aer ![GitHub stars](https://img.shields.io/github/stars/Qiskit/qiskit-aer?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F20-blue?style=flat)

### NVIDIA cuQuantum
状態ベクトル(cuStateVec)・テンソルネットワーク(cuTensorNet)・密度行列シミュレーション用 GPU ライブラリ。Qiskit Aer、Cirq/qsim、PennyLane、CUDA-Q のバックエンドとして利用。

- https://developer.nvidia.com/cuquantum-sdk
- https://github.com/NVIDIA/cuQuantum ![GitHub stars](https://img.shields.io/github/stars/NVIDIA/cuQuantum?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F10-blue?style=flat)

### Qulacs
日本発(大阪大学・QunaSys 由来)の高速な C++/Python 変分量子回路シミュレータ。

- https://github.com/qulacs/qulacs ![GitHub stars](https://img.shields.io/github/stars/qulacs/qulacs?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F29-blue?style=flat)

### qsim / QuEST
Cirq と統合された Google の最適化状態ベクトルシミュレータ(qsim)；オックスフォード発のマルチスレッド・分散・GPU 対応シミュレータ(QuEST)。

- https://github.com/quantumlib/qsim ![GitHub stars](https://img.shields.io/github/stars/quantumlib/qsim?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F06%2F24-blue?style=flat)
- https://github.com/QuEST-Kit/QuEST ![GitHub stars](https://img.shields.io/github/stars/QuEST-Kit/QuEST?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F24-blue?style=flat)

### QuTiP
Python 用量子ツールボックス。開放量子系・マスター方程式・量子光学・パルスレベルのダイナミクス。

- https://qutip.org/
- https://github.com/qutip/qutip ![GitHub stars](https://img.shields.io/github/stars/qutip/qutip?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F04-blue?style=flat)

### quimb / ITensors.jl
量子情報・回路シミュレーション・多体物理(DMRG、MPS、PEPS)向けテンソルネットワークライブラリ。Python(quimb)と Julia(ITensors.jl)。

- https://github.com/jcmgray/quimb ![GitHub stars](https://img.shields.io/github/stars/jcmgray/quimb?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F10-blue?style=flat)
- https://github.com/ITensor/ITensors.jl ![GitHub stars](https://img.shields.io/github/stars/ITensor/ITensors.jl?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F27-blue?style=flat)

---

## 誤り訂正・エラー緩和・誤り耐性

量子誤り訂正(QEC)研究、現在のノイズのある実機でのエラー緩和、誤り耐性アルゴリズムのリソース見積もりのためのツール。

### Stim / PyMatching
QEC 実験向けの非常に高速なスタビライザ回路シミュレータ・サンプラ(Stim)；表面符号などの QEC 符号用の最小重み完全マッチングデコーダ(PyMatching)。

- https://github.com/quantumlib/Stim ![GitHub stars](https://img.shields.io/github/stars/quantumlib/Stim?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F05%2F22-blue?style=flat)
- https://github.com/oscarhiggott/PyMatching ![GitHub stars](https://img.shields.io/github/stars/oscarhiggott/PyMatching?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F09%2F25-blue?style=flat)

### Mitiq
Unitary Foundation によるエラー緩和ツールキット(ゼロノイズ外挿、確率的エラー打ち消しなど)。主要な量子 SDK・実機に対応。

- https://mitiq.readthedocs.io/
- https://github.com/unitaryfoundation/mitiq ![GitHub stars](https://img.shields.io/github/stars/unitaryfoundation/mitiq?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F04-blue?style=flat)

### Qualtran
誤り耐性量子アルゴリズムを記述・解析する Google のライブラリ。量子ビット数・T ゲート数などのリソース見積もりを含む。

- https://github.com/quantumlib/Qualtran ![GitHub stars](https://img.shields.io/github/stars/quantumlib/Qualtran?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F01%2F22-blue?style=flat)

---

## 最適化と量子アニーリング

組合せ最適化(スケジューリング、配送経路、設計最適化)向けの QUBO / イジング定式化、量子アニーラ、量子インスパイアドソルバ。

### D-Wave Ocean SDK
問題の定式化(BQM/CQM、dimod)と、D-Wave の量子アニーラ・ハイブリッドソルバ・古典サンプラでの求解を行う Python ツール群。

- https://docs.dwavequantum.com/
- https://github.com/dwavesystems/dwave-ocean-sdk ![GitHub stars](https://img.shields.io/github/stars/dwavesystems/dwave-ocean-sdk?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F09%2F15-blue?style=flat)

### OpenJij / PyQUBO
日本発のオープンソース Ising/QUBO フレームワーク。シミュレーテッドアニーリング・シミュレーテッド量子アニーリングを搭載(OpenJij、Jij 社)；数式から QUBO を構築する DSL(PyQUBO、リクルート)。

- https://github.com/Jij-Inc/OpenJij ![GitHub stars](https://img.shields.io/github/stars/Jij-Inc/OpenJij?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F19-blue?style=flat)
- https://github.com/recruit-communications/pyqubo ![GitHub stars](https://img.shields.io/github/stars/recruit-communications/pyqubo?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2022%2F12%2F13-blue?style=flat)

### Simulated Bifurcation
シミュレーテッド分岐アルゴリズム(東芝が提案した量子インスパイアドな Ising/QUBO ソルバ)の CPU/GPU(PyTorch)実装。

- https://github.com/bqth29/simulated-bifurcation-algorithm ![GitHub stars](https://img.shields.io/github/stars/bqth29/simulated-bifurcation-algorithm?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F04%2F10-blue?style=flat)

---

## 化学・材料・機械学習

電子状態計算、量子機械学習、サンプリングベース手法のためのアプリケーションライブラリ。

### OpenFermion / Qiskit Nature
電子状態・フェルミオン系の量子アルゴリズムをコンパイル・解析(OpenFermion)；化学・物理など自然科学の問題向け Qiskit フレームワーク(Qiskit Nature)。

- https://github.com/quantumlib/OpenFermion ![GitHub stars](https://img.shields.io/github/stars/quantumlib/OpenFermion?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F17-blue?style=flat)
- https://github.com/qiskit-community/qiskit-nature ![GitHub stars](https://img.shields.io/github/stars/qiskit-community/qiskit-nature?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F06%2F01-blue?style=flat)

### Qiskit SQD addon
サンプリングベース量子対角化(SQD)。ノイズのある量子サンプルを古典計算(しばしば HPC)で後処理し、化学問題の固有値を推定。

- https://github.com/Qiskit/qiskit-addon-sqd ![GitHub stars](https://img.shields.io/github/stars/Qiskit/qiskit-addon-sqd?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F08-blue?style=flat)

### Qiskit Machine Learning
量子カーネル・量子ニューラルネットワーク・PyTorch 連携による量子機械学習ライブラリ。

- https://github.com/qiskit-community/qiskit-machine-learning ![GitHub stars](https://img.shields.io/github/stars/qiskit-community/qiskit-machine-learning?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F08%2F19-blue?style=flat)

---

## エンジニアリング・CAE・HPC と量子

量子プロセッサと HPC センターの統合、および工学シミュレーション(CFD・偏微分方程式)向け量子アルゴリズムの研究。

### QRMI / Slurm SPANK plugins
オンプレミス/クラウドの QPU を扱うベンダー非依存の量子リソース管理インタフェース(QRMI、Rust/Python/C)と、HPC ジョブの一部として量子リソースをスケジュールする Slurm プラグイン。

- https://github.com/qiskit-community/qrmi ![GitHub stars](https://img.shields.io/github/stars/qiskit-community/qrmi?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F23-blue?style=flat)
- https://github.com/qiskit-community/spank-plugins ![GitHub stars](https://img.shields.io/github/stars/qiskit-community/spank-plugins?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F21-blue?style=flat)

### OQTOPUS
クラウド量子コンピュータを運用するためのオープンソースのソフトウェア基盤(Open Quantum Toolchain for OPerators & USers)。日本(大阪大学ほか)で開発。

- https://github.com/oqtopus-team/oqtopus-cloud ![GitHub stars](https://img.shields.io/github/stars/oqtopus-team/oqtopus-cloud?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F10%2F11-blue?style=flat)

### Quantum CFD research
EU Horizon の QCFD プロジェクト(数値流体力学向け量子アルゴリズム)と、ハンブルク工科大学(TUHH)の量子 CFD 研究ページ。

- https://cordis.europa.eu/project/id/101080085 — EU CORDIS:QCFD プロジェクト
- https://www.tuhh.de/fds/research/current/qcfd — TUHH の QCFD

---

## 耐量子暗号

量子計算機を持つ攻撃者に備えた古典システムの暗号移行。

### liboqs (Open Quantum Safe)
耐量子の鍵カプセル化・署名アルゴリズム(NIST 標準の ML-KEM / ML-DSA を含む)の C ライブラリ。試作や TLS/SSH への組み込みに。

- https://openquantumsafe.org/
- https://github.com/open-quantum-safe/liboqs ![GitHub stars](https://img.shields.io/github/stars/open-quantum-safe/liboqs?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2026%2F07%2F09-blue?style=flat)

### NIST PQC
NIST の耐量子暗号標準化プロジェクト(FIPS 203/204/205)。

- https://csrc.nist.gov/projects/post-quantum-cryptography

---

## クラウド量子サービス

実機の量子コンピュータを利用できるマネージドサービス。

### Cloud platforms
QPU でジョブを実行するための主要なクラウド窓口。

- https://quantum.cloud.ibm.com/ — IBM Quantum Platform
- https://aws.amazon.com/braket/ — Amazon Braket(複数ベンダーの QPU)
- https://azure.microsoft.com/solutions/quantum-computing — Azure Quantum
- https://quantumai.google/ — Google Quantum AI
- https://www.dwavequantum.com/solutions-and-products/cloud-platform/ — D-Wave Leap(アニーリング・ハイブリッドソルバ)

---

## 学習リソース

講座・教科書・対話型チュートリアル。

### Courses & tutorials
無料の公式学習コンテンツ。

- https://quantum.cloud.ibm.com/learning — IBM Quantum Learning(Qiskit 講座)
- https://pennylane.ai/codebook — PennyLane Codebook
- https://github.com/microsoft/qdk/tree/main/katas — Microsoft Quantum Katas(QDK リポジトリ内)
- https://quantum.country/ — Quantum Country(Matuschak と Nielsen による記憶定着型エッセイ)
- https://qosf.org/ — Quantum Open Source Foundation(メンタリング、プロジェクト一覧)

---

## 関連リスト

- https://github.com/desireevl/awesome-quantum-computing ![GitHub stars](https://img.shields.io/github/stars/desireevl/awesome-quantum-computing?style=flat&label=%E2%AD%90) — 量子コンピューティングの学習・開発リソース
- https://github.com/qosf/awesome-quantum-software ![GitHub stars](https://img.shields.io/github/stars/qosf/awesome-quantum-software?style=flat&label=%E2%AD%90) — オープンソース量子ソフトウェア
- https://github.com/krishnakumarsekar/awesome-quantum-machine-learning ![GitHub stars](https://img.shields.io/github/stars/krishnakumarsekar/awesome-quantum-machine-learning?style=flat&label=%E2%AD%90) — 量子機械学習の基礎・アルゴリズム・教材
- https://github.com/artix41/awesome-quantum-ml ![GitHub stars](https://img.shields.io/github/stars/artix41/awesome-quantum-ml?style=flat&label=%E2%AD%90) — 量子機械学習の論文
- https://github.com/veorq/awesome-post-quantum ![GitHub stars](https://img.shields.io/github/stars/veorq/awesome-post-quantum?style=flat&label=%E2%AD%90) — 耐量子暗号
- https://github.com/francois-marie/awesome-quantum-computing-experiments ![GitHub stars](https://img.shields.io/github/stars/francois-marie/awesome-quantum-computing-experiments?style=flat&label=%E2%AD%90) ![Release date](https://img.shields.io/badge/release-2025%2F07%2F15-blue?style=flat) — 主要な量子実験のデータベース(誤り訂正中心)
- https://github.com/poig/Qc_book_list ![GitHub stars](https://img.shields.io/github/stars/poig/Qc_book_list?style=flat&label=%E2%AD%90) — 量子コンピューティング独学用の書籍リスト
- https://github.com/shvyac/awesome-hpc ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-hpc?style=flat&label=%E2%AD%90) — HPC ツール(スケジューラ、MPI、GPU)
- https://github.com/shvyac/awesome-open-source-solvers ![GitHub stars](https://img.shields.io/github/stars/shvyac/awesome-open-source-solvers?style=flat&label=%E2%AD%90) — オープンソースの FEM/CFD/科学技術ソルバ
- https://awesome.re/ — Awesome マニフェスト

---

## shvyac の awesome リスト

[shvyac](https://github.com/shvyac) が管理しているキュレーションリストの一覧:

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
