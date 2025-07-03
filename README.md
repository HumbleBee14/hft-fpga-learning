# HFT-FPGA-Simulation: High-Frequency Trading Hardware Acceleration (Simulation Only)

This repository is focused on learning, designing, and simulating core hardware acceleration techniques used in **High-Frequency Trading (HFT)** systems using **Verilog/SystemVerilog**, **Verilator**, and **GTKWave**. The goal is to build, verify, and analyze simple trading system components entirely in simulation, showcasing how hardware can drastically reduce latency in trading pipelines.

This project is entirely simulation-based: **no physical FPGA hardware is required**.

---

## 🚀 What This Repository Covers

* Simulated design of low-latency trading pipelines (tick-to-trade)
* Market data parsing, decision logic, and order signal generation in Verilog
* Hardware-software integration concepts using Python for dummy data and visualization
* Cycle-accurate simulation and waveform analysis

---

## 🛠 Tools & Technologies Used

### 1. **Verilator** — Verilog Simulator and Compiler

* **Why:** Converts Verilog designs into cycle-accurate C++ simulators. Faster than traditional simulators and widely used in FPGA and ASIC development.
* **Install:**

```bash
sudo apt update
sudo apt install git make autoconf g++ flex bison help2man
git clone https://github.com/verilator/verilator.git
cd verilator
autoconf && ./configure
make -j$(nproc)
sudo make install
```

### 2. **GTKWave** — Waveform Viewer

* **Why:** Provides graphical visualization of simulation results (timing diagrams, signal states).
* **Install:**

```bash
sudo apt install gtkwave
```

### 3. **Python + Libraries** — Data Generation & Visualization

* **Why:** Used to generate dummy market data (packet streams) and visualize latency comparisons. Integrates with Verilator simulations.
* **Install:**

```bash
sudo apt install python3 python3-pip
pip3 install scapy matplotlib
```

### 4. **Optional: Vivado or Quartus**

* **Why:** Industry-standard FPGA development environments for actual hardware synthesis (not required for simulation).

---

## 🗄 Project Structure

```
hft-fpga-learning/
├── simulation_modules/       # Verilog modules + testbenches
├── python_utils/             # Python scripts for dummy feeds & visualization
├── waveforms/                # Output waveform files (.vcd/.fst)
├── requirements.txt
└── README.md
```

---

## 📌 Getting Started

1. Install the required tools using the commands above.
2. Clone this repository:

```bash
git clone https://github.com/HumbleBee14/hft-fpga-learning.git
cd hft-fpga-learning
```

3. Run simulation examples from `simulation_modules`.
4. Visualize outputs using `gtkwave`.

---

## ✅ Key Concepts Explored

* Market data parsing (binary protocols)
* Real-time decision making in hardware
* Signal generation and minimal latency response
* Hardware/software co-design (Verilog + Python)

---

## 📚 Recommended Background Knowledge

* Basic Verilog/SystemVerilog
* Digital design fundamentals (FSMs, pipelining)
* Networking basics (UDP, TCP packet structures)
* High-Frequency Trading system architecture (optional)

---

## 🤝 Contributions & License

Contributions are welcome. Please open issues or pull requests for improvements or suggestions.

Licensed under MIT License.

