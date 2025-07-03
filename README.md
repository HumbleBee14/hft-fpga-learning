# HFT-FPGA-Simulation: High-Frequency Trading Hardware Acceleration (Simulation Only)

This repository is focused on learning, designing, and simulating core hardware acceleration techniques used in **High-Frequency Trading (HFT)** systems using **Verilog/SystemVerilog**, **Verilator**, and **GTKWave**. The goal is to build, verify, and analyze simple trading system components entirely in simulation, showcasing how hardware can drastically reduce latency in trading pipelines.

This project is entirely simulation-based: **no physical FPGA hardware is required**.

---

## 🎯 Learning Objective

**Learning Low Latency, Systems level understanding from both software and hardware perspective!**

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

## 📖 Learning Resources & References

### 🔗 Essential Reading

#### FPGA & Hardware Design
* [FPGA Programming for Beginners](https://www.fpga4fun.com/) - Excellent starting point for FPGA concepts
* [Verilog Tutorial](https://www.chipverify.com/verilog/verilog-tutorial) - Comprehensive Verilog guide
* [Digital Design and Computer Architecture](https://www.amazon.com/Digital-Design-Computer-Architecture-Harris/dp/0123944244) - Foundational textbook

#### High-Frequency Trading & Low Latency
* [Building Low Latency Applications with C++](https://www.packtpub.com/product/building-low-latency-applications-with-c/9781837639359) - Software perspective
* [FPGA-based High-frequency Trading](https://ieeexplore.ieee.org/document/6851876) - Academic paper on HFT acceleration
* [Market Data Protocols](https://www.cmegroup.com/confluence/display/EPICSANDBOX/MDP+3.0+-+Market+Data+Platform) - Understanding market data formats

### 🎥 Video Resources
* [Ben Eater's Digital Electronics Playlist](https://www.youtube.com/playlist?list=PLowKtXNTBypGqImE405J2565dvjafglHU) - Hardware fundamentals
* [Nandland FPGA Tutorials](https://www.youtube.com/c/Nandland) - FPGA and Verilog tutorials
* [HFT Explained](https://www.youtube.com/watch?v=d8BcCLLX4N4) - Trading system overview

### 🛠 Tools & Documentation
* [Verilator Documentation](https://verilator.org/guide/latest/) - Official Verilator guide
* [GTKWave User Guide](http://gtkwave.sourceforge.net/gtkwave.pdf) - Waveform analysis
* [SystemVerilog Reference](https://www.systemverilog.io/) - Language reference

### 📊 Industry Insights
* [FPGA Journal](https://www.fpgajournal.com/) - Industry news and applications
* [Trading Technology](https://www.tradingtechnologies.com/blog/) - HFT technology blog
* [Xilinx Application Notes](https://www.xilinx.com/support/documentation-navigation/application-notes.html) - Real-world FPGA applications

### 🔬 Research Papers
* "Ultra-Low Latency Trading Systems" - Survey of techniques
* "FPGA Acceleration of Financial Applications" - Implementation strategies
* "Network Processing on FPGAs" - Packet processing optimization

### 💡 Practical Examples
* [OpenCores](https://opencores.org/) - Open-source hardware designs
* [FPGA4Student](https://www.fpga4student.com/) - Practical FPGA projects
* [Altera/Intel FPGA Examples](https://www.intel.com/content/www/us/en/programmable/support/support-resources/design-examples.html)

### 🔍 Additional References & Community Resources

Any relevant posts, blogs, forum discussions, and other useful links I found:

* [FPGA in HFT - Reddit Discussion](https://www.reddit.com/r/FPGA/comments/1jh4vmn/fpga_in_hft/) - Community discussion on FPGA applications in high-frequency trading
* [FPGA Comment on Trading Applications](https://www.reddit.com/r/FPGA/comments/1bejcwg/comment/kutsmq1/) - Insightful comment about FPGA trading implementations
* [High Frequency Trading with FPGAs](https://www.youtube.com/watch?v=iwRaNYa8yTw) - Video explanation of FPGA use in HFT
* [FPGA Trading Systems Deep Dive](https://www.youtube.com/watch?v=JmVOEkskft4) - Technical video on FPGA trading architectures
* [HFT Interview Questions & Concepts](https://thedatabus.in/hft_interview) - Interview preparation and key HFT concepts




---

## 🤝 Contributions & License

Contributions are welcome. Please open issues or pull requests for improvements or suggestions.

Licensed under MIT License.

