# Download

## V3.2.2

Neptune Prover 3.2.2 GPU Operation Configuration Guide

GPU Memory Classification and Startup Methods

Based on single GPU memory size, configurations are divided into three categories:

🚀 Category 1: High Memory Configuration (>40GB)

- ​Memory Requirement: Single GPU memory greater than 40GB
- Multi-GPU Support: ✅ Supported
- CPU Configuration: 1 GPU corresponds to 1 CPU core
​- Startup Parameter: `-m 0`

⚡ Category 2: Medium Memory Configuration (>24GB)

- ​Memory Requirement: Single GPU memory greater than 24GB
- Multi-GPU Support: ✅ Supported
- CPU Configuration: 1 GPU corresponds to 1 CPU core
- Startup Parameter: `-m 1`

🔧 Category 3: Basic Memory Configuration (>4GB)

- ​Memory Requirement: Single GPU memory greater than 4GB
- Multi-GPU Support: ✅ Supported
- CPU Dependency: ⚠️ Strong dependency on CPU performance
- Startup Parameter: `-m 2`
- Performance Optimization: Adjust concurrent tasks via environment variable `export RUN_TASKS=n  # n × 4 must be less than GPU memory (GB)`

Fix 64GB Memory Crash

GPU Performance Data
-	NVIDIA GeForce RTX 3090 : 6.5 M
-	NVIDIA GeForce RTX 4070 : 11.8 M
-	NVIDIA GeForce RTX 5090 : 22 M


GPU

**NPT**
- **ubuntu**: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/v2/ubuntu_20-dr_neptune_prover-3.2.2.tar.gz


## V3.2.1
Part 1 Use GPU(Generate GuesserBuffer):
-	NVIDIA GeForce RTX 4070 Ti SUPER  28s
-	NVIDIA GeForce RTX 3090           43s

<img width="1082" height="626" alt="image" src="https://github.com/user-attachments/assets/4ffaf4a3-b18a-424a-a243-89da744d1738" />


CPU + GPU（option）

**NPT**
- **ubuntu 20**: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/v2/ubuntu_20-dr_neptune_prover-3.2.1.tar.gz
- **ubuntu 24.04 avx512**: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/v2/ubuntu_24_avx512-dr_neptune_prover-3.2.1.tar.gz

## V3.2.0
- **3.2.0 CPU+GPU**:​ Compared to v3.1.0, it represents a 100%～200% improvement;


CPU + GPU（option）

**NPT**
- **ubuntu 20**: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/v2/ubuntu_20-dr_neptune_prover-3.2.0.tar.gz
- **ubuntu 24.04 avx512**: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/v2/ubuntu_24_avx512-dr_neptune_prover-3.2.0.tar.gz

## V3.1.0

CPU+GPU proof generation achieves 5-10x speed acceleration.

CPU + GPU（option）

**NPT**
- **ubuntu 20**: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/v2/ubuntu_20-dr_neptune_prover-3.1.0.tar.gz
- **ubuntu 24.04 avx512**: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/v2/ubuntu_24_avx512-dr_neptune_prover-3.1.0.tar.gz
