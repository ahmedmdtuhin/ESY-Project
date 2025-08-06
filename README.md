# Embedded Systems Lab Project – LT16x32 SoC Extension with CAN-Based Synchronization

This repository documents a master's project conducted as part of the **Embedded Systems Lab** at TU Kaiserslautern from **October 2022 to March 2023**.

## 📌 Project Overview

The project focuses on extending the **LT16x32 softcore CPU** by integrating custom hardware peripherals, interrupt service routines, and a distributed system communication protocol using the **CAN bus**.

Key deliverables included:
- Designing new I/O peripherals (e.g., CAN Frame Generator, Scrolling Interface Generator).
- Implementing a memory-mapped I/O system using the **Wishbone bus**.
- Writing and testing interrupt service routines for real-time system control.
- Partitioning system functionality across hardware and software.
- Building a distributed **CAN-based synchronization system** between multiple nodes (clients).
- Ensuring low-latency synchronization of a dataset across all clients.
- Displaying node status and messages on a **scrolling 7-segment interface**.

> ⚠️ **Note**: The source code for this project is **not publicly available** in this repository. Code and implementation details can be shared **upon request**.

## 🧩 System Architecture

- **Processor**: LT16x32 softcore RISC CPU.
- **Bus**: Wishbone memory-mapped communication bus.
- **Peripherals**:
  - **CAN Frame Generator** – Generates CAN messages from button/switch inputs.
  - **Scrolling Interface Generator** – Handles dynamic 7-segment display updates.
  - **IRQ Mask & Timers** – Prevents race conditions and manages write cycles using timers t1 and t2.
- **Software**:
  - Interrupt Handlers (IRQn1, IRQn2, IRQ3) for managing CAN transmission, reception, and display updates.

## 🌐 Communication System

A real-time, **CAN bus-based distributed system** was implemented with:
- Three FPGA-based nodes.
- Synchronization of data packets between nodes.
- Conflict management using busy flags and timers.
- Visual feedback via scrolling segment displays.
- System verified through simulation and demonstration phases.

## 👨‍💻 Authors & Contributions

- **Interrupt Handlers (Software)**: Zimin  
- **CAN Frame Generator (Hardware)**: Napatsorn  
- **Scrolling Interface Generator (Hardware)**: Md Tuhin Ahmed  
- **IRQ Mask and Timers (Hardware)**: Kamal  
- **Simulation & Verification**: All members

---

📁 *This repository currently contains only the project PDF.*  
For source code or additional materials, please **contact the author**.

**Author**: Md Tuhin Ahmed  
**Email**: [ahmedmd.tuhin@yahoo.com](mailto:ahmedmd.tuhin@yahoo.com)