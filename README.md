# Low Power CMOS Digital Integrated Circuit Design and Physical Verification Suite

This repository contains the complete laboratory implementation and design flow for the ELE734 – Low Power Digital Integrated Circuits course. The project progressively develops CMOS digital circuits starting from fundamental MOSFET device characterization and transistor-level analysis, eventually expanding into complete CMOS logic families and a physically verified 1-bit full adder implementation. The overall work heavily focuses on low-power CMOS design methodology, transistor sizing, logical effort analysis, parasitic-aware circuit behavior, and full custom VLSI physical design using the Cadence Virtuoso environment.

The complete project was developed through a full-custom IC design flow involving:

* Schematic design
* Device-level simulation
* CMOS logic implementation
* Physical layout design
* DRC/LVS verification
* Parasitic extraction (PEX/PVE)
* Post-layout transient analysis

The labs collectively demonstrate how theoretical CMOS behavior compares against practical real-world circuit operation once parasitic capacitances, routing resistance, layout geometry, and short-channel effects are introduced into the system.

---

# Project Overview

The project begins with the analysis of NMOS and PMOS transistor characteristics and gradually transitions into increasingly complex CMOS digital systems. Throughout the labs, circuits were designed and verified using:

* Cadence Virtuoso
* ADE L simulation environment
* Calibre DRC/LVS/PEX verification flow

The work explores both ideal theoretical CMOS behavior and practical extracted post-layout behavior, emphasizing the importance of physical effects in modern low-power VLSI systems.

Key concepts explored throughout the project include:

* CMOS inverter design and sizing
* MOSFET I-V characteristics
* Subthreshold conduction
* Body effect
* Channel length modulation
* Noise margins
* CMOS logic families
* Logical effort optimization
* Rise/fall delay balancing
* High-skewed and low-skewed logic
* Physical layout parasitics
* Delay analysis
* Full-custom layout verification

---

# Lab 1 – MOSFET Device Characteristics and Physical Verification

The first stage of the project focused on understanding the characteristics and behaviors of NMOS and PMOS transistors at both the schematic and layout levels.

The lab introduced:

* NMOS and PMOS schematic creation
* Symbol generation
* Layout implementation
* Testbench construction
* DRC and LVS verification
* Parasitic extraction workflows

Multiple transistor characteristics were analyzed using Cadence simulation environments, including:

* IDS-VDS characteristics
* IDS-VGS curves
* Subthreshold conduction
* Threshold voltage variation
* Body effect behavior

The simulations demonstrated how:

* Drain current increases linearly in the triode region
* Current enters saturation beyond (V_{DS} = V_{GS} - V_{TH})
* Subthreshold conduction exists even before threshold voltage is reached
* Threshold voltage increases with source-to-body bias due to body effect

The extracted post-layout simulations further demonstrated how:

* Interconnect parasitics
* Layout geometry
* Additional resistances and capacitances
* Channel length modulation

all contribute to deviations from ideal transistor behavior.

This lab established the complete foundation for later CMOS circuit design and low-power analysis.

---

# Lab 2 – CMOS Inverter Design and Delay Analysis

The second stage focused on designing and analyzing a CMOS inverter using both theoretical transistor sizing and practical schematic/layout simulations.

The project explored:

* CMOS inverter voltage transfer characteristics
* Switching threshold analysis
* Beta ratio optimization
* Skewed inverter behavior
* Propagation delay derivation
* Noise margin behavior

The inverter was theoretically designed using:

* Long-channel square-law MOSFET models
* Mobility equations
* Oxide capacitance calculations
* Saturation current analysis

NMOS and PMOS widths were calculated analytically to achieve balanced rise/fall delays and an inverter threshold near (V_{DD}/2).

The lab further investigated:

* HI-skewed inverters
* LO-skewed inverters
* Transition voltage shifting
* PMOS/NMOS drive strength balancing

Physical implementation included:

* CMOS inverter schematic design
* Layout generation
* DRC/LVS verification
* PEX extraction
* Post-layout transient simulations

One of the major observations from this lab was the discrepancy between theoretical ideal behavior and practical extracted behavior. The extracted simulations revealed:

* Reduced voltage gain
* Longer propagation delays
* Switching threshold shifts
* Asymmetrical transitions

caused by:

* Short-channel effects
* Velocity saturation
* Contact resistance
* Routing parasitics
* Interconnect capacitances

The work demonstrated that modern CMOS circuits require parasitic-aware design methodologies rather than purely ideal theoretical sizing.

---

# Lab 3 – CMOS Logic Families (NAND/NOR Design)

The third stage expanded the design process into CMOS logic gates, specifically:

* NAND2 gates
* NOR2 gates

The lab focused heavily on transistor sizing methodologies and skew optimization techniques.

Three logic configurations were analyzed:

* Unskewed gates
* High-skewed gates
* Low-skewed gates

Theoretical logical effort analysis was performed to compare:

* Rising delay
* Falling delay
* Average logic effort

for each skew configuration.

The project implemented:

* NAND2 schematics
* NOR2 schematics
* Layout designs
* PEX extracted layouts
* Schematic vs extracted comparisons

Extensive transient simulations were conducted while sweeping load capacitances from:

* 0 fF to 150 fF

The results demonstrated:

* High-skewed gates switch faster on rising transitions
* Low-skewed gates switch faster on falling transitions
* Unskewed gates maintain balanced propagation behavior

The extracted post-layout simulations showed that:

* Parasitic capacitances
* Diffusion capacitance
* Routing resistance
* Gate overlap capacitance

introduced small increases in propagation delay while preserving the original functional behavior.

One of the strongest conclusions from this lab was the high consistency between:

* Pre-lab theory
* Schematic simulation
* Physical extracted simulation

showing that the physical layouts accurately preserved the intended CMOS logic behavior.

---

# Lab 4 – CMOS 1-Bit Full Adder Design

The final stage of the project implemented a complete CMOS 1-bit full adder using NAND-based CMOS logic.

The design process involved:

* Boolean logic derivation
* Truth table verification
* Logical effort optimization
* Multi-stage path sizing
* Capacitive load analysis
* Full custom physical implementation

The SUM and COUT equations were implemented using optimized CMOS logic networks:

* (S = A \oplus B \oplus C_{in})
* (C_{out} = AB + (A \oplus B)C_{in})

Logical effort methodology was heavily used to:

* Minimize propagation delay
* Determine optimal stage effort
* Calculate transistor widths
* Optimize path effort across all NAND stages

The complete design flow included:

* Gate-level schematic implementation
* Testbench validation
* Transient response analysis
* Full layout routing
* DRC verification
* LVS verification
* PEX extraction
* Post-layout simulation comparison

The post-layout simulations demonstrated that:

* Functional behavior remained fully correct
* SUM and COUT outputs matched expected truth-table behavior
* Timing delays slightly increased due to parasitic loading
* Waveform structures remained preserved despite layout-induced delay

The extracted simulations clearly showed the impact of:

* Interconnect capacitance
* Physical routing resistance
* Real layout parasitics

while validating that the full-adder design remained reliable and physically accurate.

---

# Key Technical Skills Used:

* CMOS transistor-level circuit design
* Low-power digital integrated circuit analysis
* Cadence Virtuoso custom IC design flow
* DRC/LVS physical verification
* PEX and post-layout simulation
* MOSFET device characterization
* Logical effort optimization
* CMOS inverter sizing
* NAND/NOR gate implementation
* Full custom VLSI layout design
* Delay and timing analysis
* Parasitic-aware CMOS design
* Physical design verification methodologies
* Analog and digital simulation workflows

---

# Conclusion:

This project demonstrates a complete progression from fundamental MOSFET analysis to fully verified CMOS digital system implementation. Across all four labs, theoretical transistor behavior, schematic simulations, and extracted post-layout simulations were continuously compared to evaluate how practical layout effects influence circuit performance.

The work highlights the importance of:

* Realistic device modeling
* Layout-aware circuit design
* Parasitic extraction
* Timing optimization
* Physical verification

in modern low-power VLSI systems.

Overall, the project establishes a strong foundation in CMOS digital integrated circuit design, custom physical layout implementation, and practical semiconductor device analysis using industry-standard EDA methodologies.

