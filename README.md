This repository contains Grasshopper definitions and associated G-code generation logic used in the development of a bio-inspired, passively actuated responsive skin. The project translates biomechanical principles of cardiac tissue into programmable material logic using multi-material additive manufacturing.

## 🧠 Project Overview

This work explores a novel fabrication strategy that merges biological inspiration with architectural innovation. Drawing on the contraction mechanics and tissue architecture of the human heart, a responsive skin is designed using three materials with distinct properties:

The toolpaths were customized in Grasshopper to embed material-specific logic, enabling the production of complex deformations with a single, efficient G-code output.

- **LayWoodMeta5**: Hygroscopic, responsible for passive actuation.
- **PLA**: Provides structural support and bending resistance.
- **TPU**: An elastic layer functioning analogously to the extracellular matrix (ECM), controlling and guiding deformation.

## 🛠️ Contents

- `24_04_26_ GCode extruder and CNC clean.gh`: Final version for G-code optimization and multi-material printing.
- `23_11_10_ Toolpath.gh`: Toolpath generation logic based on unit geometry and material behavior.
- `23_11_07_ Gcode cleaned.gh`: Early iteration of G-code cleaning and preparation pipeline.

## ✨ Key Features

- **Homemade Toolpath Generator**: Custom logic for printing responsive units with active, passive, and elastic layers.
- **Multi-Material Support**: Optimized for PLA, LayWoodMeta5, and TPU printing in a single G-code output.
- **Biomimetic Deformation**: Emulates heart tissue structure and behavior to achieve heterogeneous, reversible, and scalable deformation patterns.
- **Embedded Logic**: Material order, density, and sequence are encoded geometrically and computationally.

## 📦 Requirements

- **Software**: Rhino 3D + Grasshopper
- **Plugins**: 
- **Hardware**: 3D printer, filament material, CNC if going for larg scale printing and aim to use GCode extruder and CNC.gh

## 🚀 How to Use

1. Open the `.gh` file in **Grasshopper**.
   
### 1. Toolpath Generator (`Toolpath Generator.gh`)
- The geometry for responsive tiles is embedded in the initial `Curve` component.
- Adjust parameters:
  - Layer count
  - Tile geometry
- ⚠️ If using more than one layer per material, ensure curves across layers are properly connected.

### 2. G-code Generator (`Gcode Generator.gh`)
- Import your own curves or use those generated in Step 1.
- Adjust G-code settings (e.g., feed rate, temperature).
- Set the material sequence by identifying switch points in the toolpath.
- Copy the output G-code from the panel or use export tools to save the final `.gcode` file.

### 3. G-code & CNC Export (`Gcode and CNC.gh`)
- Follow the same G-code generation logic.
- In addition to extruder G-code, this file allows exporting CNC paths (for subtractive fabrication or hybrid workflows).

## 📚 Further Reading & Related Work

For deeper insights into the fabrication methodology and background research, see:
- **“Woven Elastic Interlayer for 3D‑Printed Hygroscopic Tiles”**  

## 🙏 Acknowledgements

- Julia Barnoin, Lead researcher
- NSF URoL:EN Grant
- Sabin Design Lab (Architecture, Cornell University)
- Butcher Lab (Biomedical Engineering, Cornell University)

## ✉️ Contact

For questions or collaborations, please reach out via GitHub or institutional email.
