# Download

## V3.3.0

### **Version Release Notes**

This update focuses on performance enhancements, introduces new output display units, and expands the `-m`parameter options for greater configuration flexibility .

**1. Key Updates**

- **Performance Optimization**: General performance improvements have been implemented .
- **Support for Displaying Output in Megabytes (M)**: Output can now be displayed in megabytes for clearer data reading.
- **Extended `-m`Parameters**: Additional memory modes have been added to accommodate different hardware configurations .

**2. Detailed `-m`Parameter Specifications**

The following table details the available `-m`parameter modes :

| Parameter   | Resource Allocation | VRAM Requirement Description                                 |
| ----------- | ------------------- | ------------------------------------------------------------ |
| **`-m 0`**  | GPU-only            | Requires **over 40GB** of VRAM                               |
| **`-m 1`**  | GPU-only            | Requires **over 30GB** of VRAM                               |
| **`-m 2`**  | GPU-only            | Requires **over 22.5GB** of VRAM                             |
| **`-m 3`**  | GPU-only            | Requires **over 21.25GB** of VRAM                            |
| **`-m 42`** | Hybrid (GPU + CPU)  | Allocates approx. **3GB** of VRAM per instance. Should be used with the `export RUN_TASKS=N`environment variable to optimize resources by setting the number of concurrent instances `N`, ensuring that `3 * N`does not exceed total VRAM. **The default value is `RUN_TASKS=3`**. This mode has higher requirements for PCIe bandwidth. |

**3. Migration Guide from Version 3.2.X**

- **Users of `-m 0`**: No changes are required.
- **Users running with the default parameter (no `-m`flag)**: No changes are required and will use the new default settings.
- **Previous `-m 1`users**: You may need to adjust the parameter based on your available GPU VRAM. Please evaluate and select an appropriate mode from the new options: **`-m 1`**, **`-m 2`**, or **`-m 3`**.
- **Previous `-m 2`users**: You have two recommended options:
  1. Switch to using the **`-m 42`** mode (and optionally fine-tune by setting the `RUN_TASKS`environment variable).
  2. Omit the `-m`parameter entirely to use the new **default configuration**.


**ubuntu**: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/v2/ubuntu_20-dr_neptune_prover-3.3.0.tar.gz

## V3.2.4
Fixed an issue with incorrect hash calculation on High Memory Configuration (>40GB) devices in V3.2.2.

Users with GPU memory not exceeding 40GB do not need to upgrade.

**NPT**
- **ubuntu**: https://pub-e1b06c9c8c3f481d81fa9619f12d0674.r2.dev/image/v2/ubuntu_20-dr_neptune_prover-3.2.4.tar.gz

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
