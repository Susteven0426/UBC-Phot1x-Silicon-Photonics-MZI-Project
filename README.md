# Silicon Photonics MZI Design, Fabrication & Characterization

![Platform](https://img.shields.io/badge/Platform-SiEPIC%20EBeam-blue)
![Tools](https://img.shields.io/badge/Tools-Lumerical%20%7C%20KLayout%20%7C%20Python-green)
![Status](https://img.shields.io/badge/Status-Fabricated%20%26%20Measured-brightgreen)

This repository presents an end-to-end **silicon photonics design and characterization workflow** for Mach–Zehnder Interferometers (MZIs), covering the complete development cycle from waveguide simulation, circuit modeling, layout implementation, fabrication, measurement, and data analysis.

Originally developed through the **University of British Columbia (UBC) Phot1x Silicon Photonics course**, this project was further extended into an independent design study focusing on **MZI design, compact modeling, process variation analysis, and measurement-based device validation**.

📄 **IEEE-format technical report:**  
[`MZI_Technical_Report.pdf`](./report/Silicon_Photonics_MZI_Report.pdf)

---

# 🧠 Design Flow Overview

## 1. Waveguide Simulation & Compact Modeling

- Modeled SOI strip waveguides using Lumerical MODE FDE solver.
- Extracted key optical parameters:
  - Effective index ($n_{eff}$)
  - Group index ($n_g$)
  - Optical mode profile
- Developed second-order Taylor expansion compact models for circuit-level simulation in Lumerical INTERCONNECT.

**Objective:**  
Establish accurate waveguide models to predict MZI spectral behavior and enable reliable circuit-level simulation.

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

- Designed eight MZI variants with different optical path differences:
  - ΔL = 0–250 μm
- Layout was manually designed using:
  - KLayout
  - SiEPIC EBeam PDK
- The designed devices were fabricated through the UBC Electron Beam Lithography Shuttle process for experimental characterization.

**Objective:**  
Bridge the gap between simulated photonic devices and fabricated hardware through a complete design-to-measurement workflow.

---

## 4. Experimental Data Analysis

By bridging the gap between simulation and measured device data, this project demonstrates simulation-to-measurement validation of silicon photonic devices.

Key performance metrics include:

- <2.7% deviation between simulated and measured group index.
- <0.7% FSR variation between nominally identical fabricated devices, demonstrating strong device repeatability.

Two independent approaches were developed for waveguide group index extraction:

- Simulation-based extraction using Lumerical MODE.
- Measurement-based extraction using MZI spectral characteristics.

The consistency between both approaches validates the reliability of the simulation model and measurement analysis workflow.

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

## 1. Waveguide Simulation (Lumerical MODE)

The SOI strip waveguide was simulated using Lumerical MODE FDE solver to extract optical mode properties, effective index, and group index at 1550 nm.

<img src="images/Electric_field_intensity_of_TE_mode.png" width="450">


## 2. PIC Layout Design (KLayout + SiEPIC EBeam PDK)

Eight MZI devices were designed with different optical path differences ($\Delta L$ = 0–250 μm), including FSR sweep devices, a balanced reference, and duplicate structures for repeatability analysis.

<img src="images/Layout.png" width="700">


## 3. Fabricated Device Measurement

The fabricated MZI devices were characterized using automated optical measurement. Transmission spectra were analyzed through peak detection and FSR extraction.

<img src="images/measured_spectra.png" width="700">


## 4. Group Index Extraction and Model Verification

The waveguide group index was extracted using two independent approaches:

- Direct calculation from Lumerical MODE simulation
- Experimental extraction from measured MZI FSR

The extracted values show strong agreement, validating both the compact model and measurement analysis workflow.

<img src="images/FSR_vs_invdL_meas.png" width="650">


## 5. Circuit Simulation and Measurement Comparison

The MZI circuit behavior was simulated in Lumerical INTERCONNECT using the extracted compact model and compared with fabricated device measurements.

<img src="images/Interconnect.png" width="600">
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
