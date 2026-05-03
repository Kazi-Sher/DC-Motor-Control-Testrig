# DC Motor Control Test Rig

An open-source experimental test rig for DC motor characterization and embedded control. The rig will support reproducible experiments from basic motor modeling to advanced control design.

The project is being developed as both a research portfolio artifact and a learning resource. The long-term goal is to document the hardware, firmware, datasets, model validation, and control experiments well enough that another learner can rebuild the rig and reproduce the main results. Detailed methods, equations, parameter values, and validation results are maintained in a companion technical report (forthcoming as `TECHNICAL_REPORT.md`).

## Roadmap
- [x] Hardware rig assembled and wired
- [x] Open-loop position-based model validation
- [ ] PID control
- [ ] State-space control + observer + advanced control algorithms

## Hardware

- STM32 Nucleo-F446RE microcontroller board
- 12 V DC geared motor with quadrature encoder, JGA25-371 class
- IBT-2 / BTS7960 H-bridge motor driver
- ACS712 5 A current sensor
- 12 V DC power supply

## Test Rig

<p align="left">
  <img src="images/Labelled_MotorRig.png" alt="Labeled DC motor control test rig" width="560">
</p>

## Wiring Diagram

<p align="left">
  <img src="images/MotorRig_bb.png" alt="DC motor control test rig wiring diagram" width="560">
</p>

## Repository Layout

```text
hardware/       Hardware datasheets, wiring diagram, and rig photos
firmware/       STM32 firmware, generated embedded code, board-level configuration
matlab/         MATLAB scripts/Simulink models for identification, validation, control
data/           Raw and processed experiment data used to reproduce plots/metrics
results/        Generated figures, validation plots, control outputs
docs/           Build notes, operating instructions, safety notes, method explanations
images/         README-facing images such as labeled photos and wiring diagrams
```

## Citation

If you use this project or build on the test rig design, please cite:

```bibtex
@misc{ahmed2026dcmotorcontroltestrig,
  title        = {DC Motor Control Test Rig},
  author       = {Ahmed, Kazi Sher},
  year         = {2026},
  howpublished = {\url{https://github.com/Kazi-Sher/DC-Motor-Control-Testrig}},
  note         = {Open-source hardware and control test rig}
}
```
