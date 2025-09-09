# Linux Driver with Android Integration

## Overview
This project demonstrates a **custom Linux kernel module in C** for ARM/ARM64 architecture that processes sensor events and integrates seamlessly with Android via HAL and Binder IPC. It emphasizes portability, performance, and modular Android system design.

## Features
- **Custom kernel module** capturing 100+ sensor events/sec via kernel–user interface
- Integration with **Android HAL & Binder IPC** for cross-layer communication
- Verified using **QEMU ARM64**, aligning with **Android GKI standards**
- **TCP/UDP streaming** with reliable buffer management under constrained bandwidth

## Technologies Used
- **Languages**: C (Kernel), Java/Kotlin (Android App)
- **Android Architecture**: HAL, Binder IPC mechanisms
- **Testing Tools**: QEMU ARM64 emulator
- **Protocols**: TCP/UDP networking
- **Tools**: ADB, GCC cross-compilation, Android NDK

## Getting Started

### 1. Kernel Module Setup
```bash
cd driver/
make ARCH=arm64 CROSS_COMPILE=aarch64-linux-gnu-
sudo insmod sensor_module.ko
dmesg | tail

