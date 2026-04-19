# GTFS4EV

## 📚 Documentation & Training Material

GTFS4EV is an open-source Python tool designed to support the planning of public bus electrification. By leveraging the standardized General Transit Feed Specification (GTFS), it allows planners and researchers to quickly simulate bus operations and explore electrification scenarios without requiring proprietary or vehicle-level operational data.

- 📖 [**Full Documentation**](https://gtfs4ev.github.io/gtfs4ev/): Full user guide, API, and methodology
- 💻 [**Project GitHub**](https://github.com/gtfs4ev/gtfs4ev): Source code, examples
- 🐍 Language: Python 3.12

---

## 🧠 Model Overview

The model allows to quickly simulate bus operations and explore electrification scenarios using GTFS data as the main input. It bridges the gap between detailed agent-based simulators and simplified first-order calculators, providing a modular workflow for GTFS data pre-processing, fleet operation and charging simulation, and ex-post analysis of electrification impacts (CO2 savings, reduction of exposure to air pollution, fuel cost savings) and the potential integration of photovoltaic energy.

The core functionality of GTFS4EV spans three main dimensions, which together form also the high-level simulation workflow:

1. GTFS data pre-processing: GTFS data validation and cleaning.
2. Fleet operation simulation: Data-based simulation of bus fleet operations, estimating the number of vehicles in operation and their travel patterns.
3. Scenario-based charging: Spatio-temporal charging demand, scenario feasibility, and infrastructure requirements (required number of chargers, required bus battery capacities) under user-defined electrification scenarios (i.e., available charging powers, charging strategy, and electric bus energy consumption)

---

## ⚙️ Installation

### 🐍 Python Setup

We recommend using **Miniconda**:
- Install [Miniconda](https://docs.conda.io/en/latest/miniconda.html) and create a virtual environment:

```bash
conda create --name evpv-env python=3.12
conda activate gtfs4ev-env
```

### 📦 Install GTFS4EV

```bash
pip install gtfs4ev
```

---

## ▶️ How to GTFS4EV

### 🔹 Step 1: Prepare Your Config File and GTFS data
- Copy and adapt the [cli_basic.py](https://github.com/gtfs4ev/gtfs4ev/tree/main/examples) example configuration file
- Make sure you have GTFS data that contains all the files required by GTFS4EV

### 🔹 Step 2: Run the CLI Model
```bash
gtfs4ev
```
Then enter the path to your config file when prompted.

### ⚠️ Notes:
- Use **absolute paths** or launch the terminal in the config file directory
- Recommended: Start by running the **example** to familiarize yourself with inputs and outputs

---

## 🧪 Advanced Usage

Import GTFS4EV modules into your own scripts:
```python
from gtfs4ev.core.gtfsmanager import GTFSManager
from gtfs4ev.core.fleetsimulator import FleetSimulator
from gtfs4ev.core.chargingsimulator import ChargingSimulator
```
All classes are described in the [API Reference](https://gtfs4ev.github.io/gtfs4ev/api/package-structure/) of the full documentation.

---

## ⭐ Other standout features 

* GTFS data filtering (e.g. suppression of specific services) or enrichment (e.g. addition of extra idle times at stops or terminals).
* PV integration potential: Assess charging demand alignment with local solar PV generation.
* Ex-post impact analysis (CO₂ savings, spatial air pollution reduction, and fuel cost savings).
* Flexible charging strategy support: Includes built-in charging strategies with also the option for users to implement custom strategies.
* Supports multiple charging strategies applied in sequence. The model starts with the first strategy and falls back to the next one if charging needs are not met. This approach allows building a complex charging logic by layering simpler strategies without needing to rewrite or duplicate code.
* Spatial visualization of transport network and charging demand as HTML maps 
* Dual usage: Use as a CLI or as a modular Python library for advanced analysis.

---

### ❓ Need Help?

Check our [Questions & Answers](docs/faq.md) page for common issues and guidance.

---

## 📜 License

Distributed under the [GNU GPLv3](https://www.gnu.org/licenses/gpl-3.0.html).
Originally developed under the lead of EPFL PV-LAB (Switzerland). Authors involved: Jérémy Dumoulin, Alejandro Peña-Bello, Noémie Jeannin, Nicolas Wyrsch.
Now under the maintenance of the [African Energy Modelling Network](https://africanenergymodellingnetwork.net/en/home).


