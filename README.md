# Custom 8-bit CPU Project

## 📜 Overview
This project is a ground-up design of a custom 8-bit computer system. It encompasses the entire computing stack: from silicon-level gate logic and a custom Instruction Set Architecture (ISA) to a physical custom PCB and a lightweight software ecosystem.

The goal is to create a fully standalone computing platform capable of running a custom operating system and user-defined programs.

---

## ⚙️ Core Specifications

### Central Processing Unit
* **Data Bus:** 8-bit
* **Address Bus:** 24-bit (supporting up to 16 MB of memory)
* **Clock Speed:** Target ~2 MHz
* **Architecture:** Custom ISA with a focus on modularity

### Memory Map
* **Base RAM:** 512 KB
* **Max Addressable RAM:** 16 MB
* **I/O Model:** Planned memory-mapped I/O for peripherals

### Display & Audio
* **Display:** 480 × 320 LCD via RGB332 (8-bit color)
* **Audio:** Software-generated square wave mixing via an onboard buzzer

---

## 🛠 Hardware & Manufacturing Flow

The transition from logic design to physical hardware follows a rigorous EDA (Electronic Design Automation) pipeline:

1. **Logic Design:** Prototyped and verified in **Digital** (by H. Neemann).
2. **Hardware Description:** Logic converted to **VHDL** for synthesis.
3. **Silicon Layout:** Synthesized to **GDSII** using the **OpenLANE** flow.
4. **System Integration:**
    * **Custom PCB:** A bespoke circuit board designed to interface the CPU with memory and peripherals.
    * **Power System:** Integrated **Lithium battery** management (planned) for portable operation.

---

## 💾 Software & Bootloader

* **Bootloader:** Stored in EEPROM; handles hardware initialization and OS loading.
* **Storage:** Parallel Flash-based cartridges for program and game storage.
* **Operating System:** A lightweight, text-based OS (Planned), inspired by Game Boy-style efficiency.
* **Drivers:** Dedicated low-level drivers for Framebuffer management and Audio synthesis.

---

## 🚀 Project Roadmap

- [x] Initial CPU Logic Design (Digital)
-  VHDL Conversion & Verification (In Progress)
- [ ] GDSII Physical Layout (OpenLANE)
- [ ] Custom PCB Design & Fabrication
- [ ] Lithium Battery Power Circuitry
- [ ] OS Kernel Development
- [ ] Video/Audio Driver Implementation

---

## ⚖️ License

**Copyright (C) 2026 Swastik Ulhas Hegde**

This project is licensed under the **GNU General Public License v3.0**. 
See the [LICENSE](LICENSE) file for the full license text.
