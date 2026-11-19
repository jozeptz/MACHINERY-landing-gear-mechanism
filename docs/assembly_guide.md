Landing Gear Mechanism

Hand-actuated, no motor. All printed parts are PLA, printed on a Creality K1 with a 0.4 mm nozzle. The backboard is 5 mm acrylic.


## 1. Overview

| Item | Detail |
|---|---|
| Mechanism | Landing gear: four-bar linkage with bell crank, driven by a piston-cylinder actuator |
| Actuation | By hand (push or pull the piston rod) |
| Joints | 6 revolute joints, each using an M3 brass pin (6 pins, 12 M3 screws; see `hardware/bom.csv`) |
| Base | Acrylic backboard, 210 x 297 mm x 5 mm |
| Related files | CAD: `hardware/mechanical/`, BoM: `hardware/bom.csv`, photos and video: `media/` |

## Kinematic reference

Labels follow the team's kinematic diagram

| Link | Part |
|---|---|
| 1 | Ground (backboard with O2, O4, O6) |
| 2 | Bell crank (pivots at O2; points C and E) |
| 3 | Actuator piston rod (C to piston B) |
| 4 | Actuator cylinder barrel (piston B to O4) |
| 5 | Coupler (from E) |
| 6 | Strut wheel (pivots at O6) |

Joints: 6 revolute (O2, C, E, the coupler-strut joint, O6, O4) and 1 prismatic (B). With 6 links and 7 lower pairs, the Gruebler count is 3(6 - 1) - 2(7) = 1 degree of freedom, so one hand-driven input (the piston rod) is enough.

## 2. Parts list

Printed (PLA): actuator cylinder barrel, actuator pedestal, actuator piston rod, bell crank, bracket O2, bracket O4, coupler, strut wheel.

Hardware: 6 x M3 brass pin, 12 x M3 screw, 1 x acrylic backboard.

Full details are in `hardware/bom.csv`.

## 3. Required tools

- Digital caliper (check printed dimensions and hole sizes)
- Hex key or screwdriver that fits the M3 screws
- Small vise or flat-jaw pliers (to press the brass pins)
- Small file or sandpaper (about 400 grit) and a hobby knife (remove elephant foot, stringing, burrs)
- Drill and 3 mm bit, or a 3 mm reamer (to clean up pin and screw holes if tight)
- Marker or labels 
- Protractor or angle gauge 

## 4. Safety notes

- Wear safety glasses when pressing pins, drilling, or sanding. Small pieces can fly off.
- Support the part when pressing a pin into it. Do not push by hand against the pin head.
- Use a hobby knife away from your body and cut on a stable surface.
- Do not overtighten screws into PLA. The threads strip easily, and tightening against acrylic can crack it.
- Acrylic edges can be sharp and acrylic can crack. Hold it by the edges with care, and do not drill close to an edge.
- Hang the finished model on a secure fixing and check that it does not tip or fall. Do not hang it over a walkway.
- Keep fingers clear of the linkage when moving it. Parts can pinch between links.

## 5. Preparation before assembly

1. Compare printed parts against the BoM. All eight printed parts must be present.
2. Clean each part: remove support material, stringing and elephant foot. File the hole edges lightly.
3. Check each joint hole with a caliper. The M3 pin should press fit in the pinned link, and turn freely in the other link. If a hole is too tight on the turning side, ream it slowly with a 3 mm bit. Do not enlarge the pressed hole.
4. Mark the links and joints with labels so they match the report.
5. Lay out all parts on the backboard in their final positions as a dry fit, before any pins go in.

## 6. Assembly

Each revolute joint follows the same three-step method: press the brass pin into one link, fit the mating link (fork link) over the pin, and fix it with an M3 screw on both sides.

### 6.1 Joint-to-parts table (fill in)

| Joint | Connects | Pin pressed into | Fork link |
|---|---|---|---|
| J1 | O2: left bracket - link 2 (bell crank) | [part] | [part] |
| J2 | E: link 2 (bell crank) - link 5 (coupler) | [part] | [part] |
| J3 | [label]: link 5 (coupler) - link 6 (strut wheel) | [part] | [part] |
| J4 | O6: right bracket - link 6 (strut wheel) | [part] | [part] |
| J5 | C: link 2 (bell crank) - link 3 (piston rod) | [part] | [part] |
| J6 | O4: actuator pedestal - link 4 (cylinder barrel) | [part] | [part] |

The piston (point B) slides inside the cylinder barrel. It is a prismatic joint, so it has no pin or screw.

### 6.2 Steps

1. **Fix the brackets to the backboard.** Mount bracket O2, the strut pivot bracket (O6) and the actuator pedestal (O4) on the acrylic backboard in the positions from the CAD. Check the distances against the drawing with a caliper. Do not fully tighten until the linkage has been assembled and moves freely. Photo: `media/[step1].jpg`
2. **Press the pins.** Press an M3 brass pin into the link that carries it, for each joint. Press straight and slowly until it is seated, with equal length protruding on the free side if the joint requires it. Photo: `media/[step2].jpg`
3. **Join the links.** Place the fork link over the pin and fit an M3 screw on each side. Tighten until snug, then back off a quarter turn if the joint does not turn freely. Repeat for each joint. Photo: `media/[step3].jpg`
4. **Assemble the four-bar linkage.** Fit the bell crank on the left bracket (J1), the coupler on the bell crank (J2), the coupler on the strut wheel (J3), and the strut wheel on the right bracket (J4). Check that each joint rotates by hand.
5. **Check clearances.** The strut wheel must clear the backboard and the brackets through the full motion.
6. **Assemble the actuator.** Insert the piston rod into the cylinder barrel, attach the barrel to the actuator pedestal (J6), and connect the rod end to the bell crank (J5). Photo: `media/[step6].jpg`
7. **Final tightening.** Move the mechanism through its full range, then tighten the bracket and pedestal fixings.

## 7. Setup and check-out

1. Move the mechanism slowly through its full range by hand. It must not bind, rub the backboard, or collide with the brackets.
2. Confirm the whole model, in every pose, stays within the 210 x 297 mm outline.
3. Record the two end positions (retracted and extended) and measure the link angles with the protractor at [4-6] intermediate positions. Save the raw data in `experiments/`, and compare with the analytical and simulation results.
4. Mount the backboard on the wall using the chosen hardware. Check that it hangs level and does not move when the mechanism is operated.

## 8. Operation

1. Start from the [retracted / gear-up] position.
2. Push (or pull) the actuator piston rod slowly and steadily by hand.
3. The bell crank turns and drives the linkage, and the strut wheel moves to the [extended / gear-down] position.
4. Reverse the rod motion to return to the start position.
5. Move gently at the end positions. Do not force the rod past the end of its travel.

Operating range: [rod stroke in mm], [angle range in degrees]. Demonstration video: `media/[Mechanism].avi`

## 9. Troubleshooting

| Problem | Likely cause | Fix |
|---|---|---|
| Joint is stiff or stuck | Hole too tight, screw too tight, or burr | Loosen the screw a quarter turn, ream the turning hole to 3 mm, remove burrs |
| Joint is loose or wobbles | Hole oversized, worn PLA | Add a thin washer, reprint the part with correct hole size |
| Pin spins in the link | Pressed hole too large | Use a drop of CA glue or reprint with a smaller hole |
| Pin will not press in | Hole too small or first layer bulge | Clean the hole with a 3 mm bit, remove elephant foot |
| Mechanism jams at one position | Link collision or misalignment | Dry-fit and check clearances, reposition the brackets |
| Piston rod binds in the barrel | Rod bent, rough print, misaligned pedestal | Sand the rod and bore lightly, realign the pedestal |
| Printed part cracks | Overtightened screw, thin wall | Replace the part, tighten less, print with more walls |
| Acrylic cracks near a hole | Overtightening or hole near an edge | Replace the backboard, use a washer, do not tighten hard |
| Model sags or leans on the wall | Weak fixing | Use a stronger fixing, add a second mounting point |
| Measured angles differ from simulation | Clearance, friction, print tolerance | Re-measure link lengths, compare with CAD values, note the cause in the report |

## 10. Maintenance

- **Before each demonstration:** move the mechanism through its full range, check that screws are snug and every joint turns freely.
- **Periodically:** look for cracks near the pins and holes, and for loose screws.
- **Cleaning:** wipe with a dry or slightly damp cloth. Do not use solvents on acrylic, because they can craze it.
- **Lubrication:** usually not needed. If friction is high, use a trace of dry lubricant such as PTFE spray. Avoid oil, which attracts dust and can attack PLA.
- **Storage:** keep away from heat (above about 50 degrees C PLA softens) and direct sunlight. Store flat or hung.
- **Spare parts:** keep the CAD and STL files in `hardware/mechanical/` so any part can be reprinted.

## 11. Photographs and diagrams

| Figure | File | Shows |
|---|---|---|
| 1 | `media/[overview].jpg` | Finished model on the wall |
| 2 | `media/[exploded].jpg` | All parts laid out |
| 3 | `media/[step1].jpg` | Brackets and pedestal on the backboard |
| 4 | `media/[step2].jpg` | Pin pressed into a link |
| 5 | `media/[step3].jpg` | Fork link with screws on both sides |
| 6 | `media/[retracted].jpg` | Retracted (gear-up) position |
| 7 | `media/[extended].jpg` | Extended (gear-down) position |

## 12. Revision history

| Version | Date | Author | Changes |
|---|---|---|---|
| 1.0 | 2026-11-19 | Gun | First version of assembly, setup, operation, troubleshooting and maintenance guide |
