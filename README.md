# UBC-Phot1x-Silicon-Photonics-MZI-Project

![Platform](https://img.shields.io/badge/Platform-SiEPIC%20EBeam-blue)
![Tools](https://img.shields.io/badge/Tools-Lumerical%20%7C%20KLayout%20%7C%20Python-green)
![Status](https://img.shields.io/badge/Status-Fabricated%20%26%20Measured-brightgreen)

This repository documents a complete **silicon photonics design flow** of Mach–Zehnder Interferometers (MZIs), from waveguide simulation and circuit modeling to tape-out, measurement, and data analysis.

The project is an extended work beyond the UBC Phot1x course, with additional focus on **process variation corner analysis**, **automated layout generation (gdsfactory)**, and **dual-method group index verification**.

> 📄 **Full technical report** (IEEE format) is available in [`report/MZI_Technical_Report.pdf`](./report/MZI_Technical_Report.pdf).

---

## 🧠 Design Flow Overview

1. **Waveguide Simulation**  
   - SOI strip waveguide modeled with **Lumerical MODE**  
   - Extracted effective index, group index, and field distribution  
   - Built 2nd-order Taylor expansion compact models for circuit simulation

2. **Circuit Simulation**  
   - MZI circuit simulated in **Lumerical INTERCONNECT**  
   - Analyzed FSR dependence on ΔL  
   - Corner analysis on waveguide width & thickness (±10 nm) for manufacturability

3. **Layout & Tape-out**  
   - 8 MZI variants with different ΔL designed in **KLayout + SiEPIC EBeam PDK**  
   - Parameterized layout scripting with **Python gdsfactory**  
   - Fabricated via UBC Electron Beam Lithography shuttle

4. **Measurement & Analysis**  
   - Custom Python/MATLAB scripts for spectral data processing  
   - Peak detection, FSR extraction, group index calculation  
   - Simulation vs. measurement comparison  
   - Device repeatability analysis across multiple dies

---

## 🔬 Key Results

### Waveguide Mode Profile (TE, 1550 nm)
![Waveguide mode](images/waveguide_mode.png)

### MZI Layout (KLayout)
![MZI Layout](images/mzi_layout.png)

### Group Index – MODE Simulation vs. FSR Extraction
![Group index comparison](images/group_index_analysis.png)

*Two independent methods converge to consistent group index values, verifying both the simulation model and the measurement extraction pipeline.*

### Measured vs. Simulated MZI Spectrum
![Measurement vs Simulation](images/measurement_vs_sim.png)

---

## 🛠 Tools & Skills Demonstrated

- **Photonics Design**: Lumerical MODE, INTERCONNECT
- **Layout**: KLayout, SiEPIC EBeam PDK, gdsfactory (Python)
- **Data Analysis**: Python (NumPy, SciPy, Matplotlib), MATLAB
- **Fabrication**: UBC EBeam shuttle, process variation awareness
- **Documentation**: IEEE-style technical report writing

---

## 📁 Repository Contents

| Folder/File | Description |
|------------|-------------|
| `report/` | Full technical report (PDF) |
| `images/` | Simulation & measurement figures |
| `scripts/` | Python analysis scripts (peak detection, FSR extraction, etc.) |
| `README.md` | This overview |

---

## 👤 About the Author

**Sheng-Xun Su (蘇聖勛)**  
M.S. in Electro-Optical Engineering, National Central University, Taiwan  
Background: semiconductor wafer fab manufacturing (3.8 years) + optical material characterization  
Career focus: **Silicon Photonics IC Design**

- 📧 [Your Email]  
- 🔗 [LinkedIn or personal website if any]

---

## 📄 License

This project is shared for portfolio demonstration under the MIT License.
