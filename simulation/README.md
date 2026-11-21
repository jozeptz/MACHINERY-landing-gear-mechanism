# Simulation

## Overview
Digital model of the Landing Gear Mechanism developed using MATLAB Simulink and Simscape Multibody. The model simulates the extension and retraction of the landing gear using a prescribed motion input.

## Files
| File / Directory | Description |
|---|---|
| `Landing_Gear.slx` | Main Simscape Multibody model |
| `../hardware/mechanical/Parts/` | Imported STEP geometry files |

## Software
- MATLAB R2026b (26.2)
- Simulink 26.2
- Simscape 26.2
- Simscape Multibody 26.2

## Simulation Settings

| Parameter | Value |
|---|---|
| Simulation time | 0–10 seconds |
| Solver type | Variable-step |
| Solver selection | Automatic |
| Relative tolerance | 1e-3 |
| Absolute tolerance | 1e-3 |
| Gravity | [0, 0, -9.80665] m/s² |
| Equation formulation | Time |
| Index reduction | Derivative replacement |

## Model Configuration
- 6 revolute joints and 1 prismatic joint.
- 6 links forming a four-bar linkage with a piston-cylinder actuator.
- Ground reference connected to the World Frame.
- CAD geometry imported through File Solid blocks.
- Components modeled as rigid bodies.

### Material Properties
| Component | Material | Manufacturing Method |
|---|---|---|
| 3D-printed mechanical parts | PLA (Polylactic Acid) | FDM 3D printing |
| Backboard | Acrylic (5 mm thickness) | Sheet fabrication |

**3D Printing Specifications:**
- Printer: Creality K1
- Nozzle diameter: 0.4 mm
- Printing material: PLA

## Results
Two 10-second simulation videos demonstrate the mechanism from different perspectives:

- [Top View](../media/videos/landingGear_Top.mp4)
- [Isometric View](../media/videos/landingGear_Iso.mp4)
