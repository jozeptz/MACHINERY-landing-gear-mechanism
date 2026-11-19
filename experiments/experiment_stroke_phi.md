# Experiment: Actuator stroke vs strut wheel angle

## Objective

Measure the strut wheel angle phi (output) against the actuator stroke s (input) on the physical prototype, and compare it with the analytical and simulation results.

## Method

1. Move the strut wheel step by step from phi = -90 deg to phi = -180 deg (about 10 deg per step).
2. At each position, mark the piston rod with a permanent marker.
3. After all positions are marked, measure the distance between the marks to get the stroke s at each position.
4. Plot phi against s and compare with the analytical s-phi curve.

## Setup, equipment and conditions

| Item | Entry |
|---|---|
| Operator | Gun |
| Date | 19/11/2026 |
| Model | 3D printed PLA landing gear, hand-actuated, 5 mm acrylic backboard |
| Orientation | flat on the table |
| Stroke measurement | Marker marks on the piston rod, distance measured with ruler |
| Angle measurement | protractor |
| Calibration status | none |
| Units | s in mm, phi in degrees |
| Analysis method | Stroke and angle pairs plotted in Excel, compared with the analytical curve |

## Results

raw data and a plot can be access in this same folder.

The measured points follow the trend of the analytical curve, but there is a noticeable difference from the simulation.

## Discussion

The difference from the simulation comes mainly from:

- **Measurement of angle and distance:** angles and mark positions were read by hand.
- **Resolution:** the resolution of the instruments and of the marker lines limits how precisely each value can be read.
- **Imperfections of the prototype:** small errors in the 3D printed parts, loose pin joints and friction mean the real model does not match the ideal dimensions.

