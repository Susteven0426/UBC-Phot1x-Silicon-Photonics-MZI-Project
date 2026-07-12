# Silicon Photonics MZI Design, Fabrication & Characterization

![Platform](https://img.shields.io/badge/Platform-SiEPIC%20EBeam-blue)
![Tools](https://img.shields.io/badge/Tools-Lumerical%20%7C%20KLayout%20%7C%20Python-green)
![Status](https://img.shields.io/badge/Status-Fabricated%20%26%20Measured-brightgreen)

This repository presents an end-to-end **silicon photonics design and characterization workflow** for Mach–Zehnder Interferometers (MZIs), covering the complete development cycle from waveguide simulation, circuit modeling, layout implementation, fabrication, measurement, and data analysis.

Originally developed through the **University of British Columbia (UBC) Phot1x Silicon Photonics course**, this project was further extended into an independent design study with additional focus on **process variation analysis, automated layout generation, and measurement-based device validation**.

📄 **IEEE-format technical report:**  
[`MZI_Technical_Report.pdf`](./report/MZI_Technical_Report.pdf)

---

# 🧠 Design Flow Overview

## 1. Waveguide Simulation & Compact Modeling

- SOI strip waveguide modeled using **Lumerical MODE**.
- Extracted key optical parameters:
  - Effective index ($n_{eff}$)
  - Group index ($n_g$)
  - Optical mode profile
- Developed second-order Taylor expansion compact models for circuit-level simulation.

**Objective:**  
Establish accurate waveguide models for predicting MZI spectral behavior.

---

## 2. Circuit Simulation & Process Variation Analysis

- MZI circuits simulated using **Lumerical INTERCONNECT**.
- Analyzed Free Spectral Range (FSR) dependence on optical path difference ($\Delta L$).
- Performed corner analysis considering fabrication variations:

  - Waveguide width variation: ±10 nm
  - Waveguide thickness variation: ±10 nm

**Objective:**  
Evaluate the impact of fabrication uncertainty on device performance and design robustness.

---

## 3. Layout Design & Fabrication

- Designed **8 MZI variants** with different optical path differences:

\[
\Delta L = 0-250 \ \mu m
\]

- Layout implemented using:

  - **KLayout**
  - **SiEPIC EBeam PDK**

- Developed parameterized layout generation workflow using:

  - **Python gdsfactory**

- Devices were fabricated through the:

  - **UBC Electron Beam Lithography Shuttle**

**Objective:**  
Bridge the gap between simulated photonic devices and fabricated hardware.

---

## 4. Measurement & Data Analysis

Developed Python and MATLAB analysis workflows for experimental characterization:

- Optical spectrum processing
- Automated peak detection
- Free Spectral Range (FSR) extraction
- Group index extraction
- Simulation versus measurement comparison
- Device repeatability analysis

---

# 🔬 Key Achievements & Results

By bridging the gap between simulation and fabrication, this project demonstrates complete **simulation-to-measurement validation** of silicon photonic devices.

Key performance metrics include:

- **<2.7% deviation** between simulated and measured waveguide group index.

- **<0.7% FSR variation** between identical fabricated devices, demonstrating strong device repeatability.

- Developed two independent approaches for waveguide group index extraction:

  1. Simulation-based extraction using Lumerical MODE.
  2. Measurement-based extraction using MZI spectral characteristics.

The consistency between both approaches validates the reliability of the simulation model and measurement analysis workflow.

---

# 📊 Technical Results

## Waveguide Mode Profile (TE Mode, 1550 nm)

![Waveguide mode](images/waveguide_mode.png)


## MZI Layout Design (KLayout)

![MZI Layout](images/mzi_layout.png)


## Group Index Validation

![Group index comparison](images/group_index_analysis.png)

Two independent extraction methods show strong agreement, validating both the simulation model and experimental analysis pipeline.


## Simulated vs. Measured MZI Spectrum

![Measurement vs Simulation](images/measurement_vs_sim.png)

The measured device response shows strong agreement with the circuit simulation results, demonstrating successful design verification.

---

# 🛠 Tools & Skills Demonstrated

## Photonic Simulation

- Lumerical MODE
- Lumerical INTERCONNECT

## PIC Layout Implementation

- KLayout
- SiEPIC EBeam PDK
- Python gdsfactory

## Data Analysis

- Python:
  - NumPy
  - SciPy
  - Matplotlib

- MATLAB

## Fabrication & Characterization

- UBC EBeam Shuttle fabrication flow
- Optical measurement analysis
- Process variation awareness
- Simulation and experimental validation

## Documentation

- IEEE-format technical report writing
- Technical data visualization

---

# 📁 Repository Contents

| Folder/File | Description |
|------------|-------------|
| `report/` | IEEE-format technical report (PDF) |
| `images/` | Simulation and measurement figures |
| `scripts/` | Python/MATLAB analysis scripts |
| `README.md` | Project overview |

---

# 👤 About the Author

**Sheng-Xun Su (蘇聖勛)**

M.S. in Electro-Optical Engineering  
National Central University, Taiwan

## Background

- 3.8 years semiconductor wafer fabrication experience
- Optical material characterization research
- Silicon photonics IC design and device characterization

## Career Focus

**Silicon Photonics IC Design | Photonic Integrated Circuits (PIC)**

Technical interests:

- Silicon photonic device design
- Photonic integrated circuits
- Optical interconnect technologies

---

# Contact

📧 Email: [Your Email]

🔗 LinkedIn: [Your LinkedIn Profile URL]


---

# License

This repository is shared for **portfolio demonstration and educational purposes**.
