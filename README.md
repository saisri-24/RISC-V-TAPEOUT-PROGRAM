# Week 0: VLSI Tool Setup

This repository documents the setup process for the essential open-source tools required for VLSI design and verification. The tools will be installed on **Oracle VirtualBox** running **Ubuntu (20.04 or later)**.

---

## 📌 System Requirements

- **Oracle VirtualBox**: [Download here](https://www.virtualbox.org/wiki/Downloads)  
- **Minimum VM Configuration**:
  - RAM: **6 GB**
  - Storage: **50 GB HDD**
  - CPU: **4 vCPUs**
  - OS: **Ubuntu 20.04+**

---

![Ubuntu using oracle](C:\Users\acer\OneDrive\Pictures\ubuntu using VM.png)

## ⚙️ Tools to Install

### 1. Yosys (Open Synthesis Suite)
bash
### Update system
sudo apt-get update

### Clone Yosys repository
git clone https://github.com/YosysHQ/yosys.git
cd yosys

### Install dependencies
sudo apt install make build-essential clang bison flex \
libreadline-dev gawk tcl-dev libffi-dev git \
graphviz xdot pkg-config python3 libboost-system-dev \
libboost-python-dev libboost-filesystem-dev zlib1g-dev

### Build Yosys
make config-gcc
make

### Install Yosys
sudo make install

---


### 2. Icarus Verilog (iverilog)

sudo apt-get update

sudo apt-get install iverilog

---

### 3. GTKWave

sudo apt-get update

sudo apt install gtkwave

---

## ✅ Verification

After installation, check versions:

yosys -V

iverilog -V

gtkwave --version

