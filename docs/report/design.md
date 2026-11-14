# 3. Detailed Mechanical Design

The selected concept was developed through four virtual iterations, each checked in SolidWorks CAD, anatomy animations and motion studies. Every iteration removed a weakness found in the one before: Design 1 (fork-lift harvester), Design 2 (two-axis gantry), Design 3 (cup holder) and the final design, Harvester_v2. The waterjet that cuts the stems is sized separately in Section 3.6. No physical prototype has been built yet; that is the work of Semester 2.

## 3.1 Design 1: Fork-Lift Harvester

### 3.1.1 Concept

Design 1 combines the fork-lift harvester with the waterjet cut from the waterjet gantry concept. The fork lifts a row of lettuce from below, a fixed waterjet cuts the stems, and a comb strips the heads into a gravity chute. The moving gantry from the waterjet concept was dropped, so the jet stays in one place. The waterjet was kept because it cuts without touching the leaves, and in other harvesting methods gripping causes most of the damage [10].

Design 1 has six components: a conveyor that indexes the trays, the fork, the fixed waterjet, a lift, stripper comb strips, and a gravity chute into a collection bin (Fig. 3.1). In one cycle the row slides onto the tines, the fork lifts it and turns 135°, and the comb strips the heads down the chute into the bin (Fig. 3.2).

<figure markdown>
  ![Design 1 in SolidWorks](../images/design/d1-solidworks.jpg){ width="900" }

  <figcaption>
    Fig. 3.1. Design 1 in SolidWorks: conveyor, fork on the lift unit, stripper comb, discharge chute and bin.
  </figcaption>
</figure>

<figure markdown>
  ![One cycle of Design 1](../images/design/d1-cycle.jpg){ width="1000" }

  <figcaption>
    Fig. 3.2. One cycle of Design 1 (anatomy model, 135° turn).
  </figcaption>
</figure>

### 3.1.2 Fork Specifications

The fork has to support each lettuce without gripping it, fit between adjacent rows and carry the full mass of the plant. Its dimensions come from published measurements of hydroponic lettuce [13] and from simulation (Table 3.1).

<div markdown style="text-align: center;">
**Table 3.1.** Fork dimensions and their basis.
</div>

| Parameter | Basis | Value |
|---|---|---|
| Tine gap (T) | Leaf spread of about 330 mm divided by 4 | ≈ 76 mm |
| Maximum tine gap | The fork must not hit lettuce in adjacent rows | T < 280 mm |
| Tine width | 14.45 ÷ 2π = 14.45 ÷ 6.283 | ≈ 23 mm |
| Tine length (L) | L ≥ 4D, where D = 79.5 mm from simulation | ≥ 318 mm (4 × 79.5 mm) |

The final design rounds the calculated values and keeps the tine length, width and gap in a ratio of 320 : 23 : 75 (Table 3.2).

<div markdown style="text-align: center;">
**Table 3.2.** Final fork dimensions.
</div>

| Dimension | Value |
|---|---|
| Tine length | 320 mm |
| Tine width | 23 mm |
| Tine gap | 75 mm |

### 3.1.3 CAD and Assembly

The fork has a steerer tube, headset cups, a crown, tines, and holes for the waterjet stream (Fig. 3.3). The parts were modelled in SolidWorks from sketches with extrude, revolve and reference-geometry features.

<figure markdown>
  ![Fork parts](../images/design/fork-parts.jpg){ width="240" style="display: inline-block;" }
  ![Fork CAD](../images/design/fork-cad.jpg){ width="440" style="display: inline-block;" }

  <figcaption>
    Fig. 3.3. Fork parts (left) and fork CAD (right).
  </figcaption>
</figure>

The assembly was built from the bottom up, with mates only where parts move. Parts that never move, such as the rotor shaft, head tubes and forks, were placed at exact coordinates and fixed.

**Lift unit.** The rotor axis and the bearing axis are coincident, so the shaft is centred in its bearings and can only spin or slide along its length. The rotor's front plane is coincident with the lift unit's front plane, which stops the sliding (Fig. 3.4). The lift unit has two positions in the simulation (Fig. 3.5, Table 3.3).

<figure markdown>
  ![Lift unit](../images/design/lift-unit.jpg){ width="800" }

  <figcaption>
    Fig. 3.4. Lift unit: rotor gearmotor, shaft, lift carriage and tines.
  </figcaption>
</figure>

<figure markdown>
  ![Lift unit at the harvest position](../images/design/lift-harvest.jpg){ width="340" style="display: inline-block;" }
  ![Lift unit at the strip position](../images/design/lift-strip.jpg){ width="340" style="display: inline-block;" }

  <figcaption>
    Fig. 3.5. Lift unit at the harvest position (left) and the strip position (right).
  </figcaption>
</figure>

<div markdown style="text-align: center;">
**Table 3.3.** Lift-unit positions in the simulation.
</div>

| | 1: Harvest | 2: Strip |
|---|---|---|
| Rotor height | 526 mm | 885 mm |
| Fork angle | Level | Turned 135° |
| During simulation | Jet cuts; heads on the forks | Heads slide off the comb |

**Frame.** In the full machine the lift unit is attached to the blue frame (Fig. 3.6). A coincident front plane stops it drifting sideways across the belt, and a coincident right plane stops it drifting along the conveyor. A distance mate sets the rotor height for each position, and a parallel mate between a rotor plane and a frame plane sets the fork angle.

<figure markdown>
  ![Blue frame carrying the lift unit](../images/design/frame.jpg){ width="700" }

  <figcaption>
    Fig. 3.6. Blue frame carrying the lift unit.
  </figcaption>
</figure>

**Interference detection.** To find places where two parts overlap, the angle plane was turned through 360° in 15° steps, which turns the fork with it. At each step the team checked whether the fork touches the frame or the stripper combs.

### 3.1.4 Problems Found in Virtual Testing

The CAD raised two questions (Fig. 3.7):

1. **Range of motor angle.** A full 360° turn lets a simple one-direction gearmotor run without position control, but the tines then sweep a full circle around the shaft, which the frame and comb must clear; this is why the interference check stepped through 360°. A 135° turn followed by reversal sweeps far less space, but needs position control, a homing sensor and two stop-and-reverse events per cycle.
2. **Comb sticking.** The comb pushes wet heads past the tines. With about 95% moisture in the leaves [13], the team expects leaves to wedge between comb and fork, a risk to be tested rather than assumed.

<figure markdown>
  ![Questions raised by Design 1](../images/design/d1-questions.jpg){ width="900" }

  <figcaption>
    Fig. 3.7. Questions raised by Design 1: the range of motor angle, and wet heads sticking between comb and fork.
  </figcaption>
</figure>

The anatomy model (Fig. 3.2) exposed three further handling problems:

- Nothing restrains the heads while the fork lifts and turns.
- The heads roll down the chute and land in a heap, whereas neat, pack-ready output is the very reason Greenphyto still harvests by hand [14].
- Every motion adds an actuator.

These findings led to Design 2.

## 3.2 Design 2: Two-Axis Gantry

Design 2 removes the turn and the comb (Fig. 3.8). A portal gantry over the end of the conveyor carries the fork on a vertical and a horizontal axis. The fork slides under the front row, the fixed jet cuts the stems, the vertical axis raises the row level, and the horizontal axis carries it over the chute, where the heads are released.

<figure markdown>
  ![One cycle of Design 2](../images/design/d2-cycle.jpg){ width="1000" }

  <figcaption>
    Fig. 3.8. One cycle of Design 2 (anatomy model, rear isometric view).
  </figcaption>
</figure>

<div markdown style="text-align: center;">
**Table 3.4.** Design 1 (one axis with a flip) compared with Design 2 (two-axis gantry).
</div>

| Aspect | Design 1: one axis + flip | Design 2: two-axis gantry |
|---|---|---|
| Motors | One lift axis plus a rotor for the flip | Two gantry axes, vertical and horizontal |
| Control | 360° continuous, or 135° with stop and reversal | Two axes must be coordinated; standard Cartesian motion |
| Head orientation | Tipped 135°; heads slide off under gravity | Level throughout |
| Release | Comb strips the heads; wet leaves may wedge | No comb; heads released over the chute |
| Swept space | Tines sweep an arc around the shaft | Rectangular envelope above the conveyor |
| Frame | Compact single portal | Larger portal with two rails |
| Remaining risks | Heads unrestrained during motion; drop into chute and bin | Same: heads unrestrained; drop into chute and bin |

Design 2 answers both questions raised by Design 1, at the cost of a second coordinated axis and a larger frame. It does not solve the main handling problem: the heads still ride loose on the tines and still drop onto a chute. The next step was therefore to ask what should hold each head while it is cut.

## 3.3 Design 3: Cup Holder

### 3.3.1 Single Cup

Design 3 replaces the open tines with a split, funnel-shaped cup that closes around the stem below the head, flanked by two S-curved rails (Fig. 3.9). As the plant advances, the rails rise and gather the outer leaves upward and inward, so the head enters the cup without being pushed or squeezed (Fig. 3.10). A rack and pinion closes the two cup halves on the stem; the jet then cuts just below the cup, leaving the stub on the conveyor while the head stays held upright.

Holding the base rather than the leaves follows the evidence on gripping damage [10], and it addresses the falling head that a tray-cutter maker reports for whole lettuce [15].

<figure markdown>
  ![Design 3 CAD](../images/design/d3-cad.jpg){ width="800" }

  <figcaption>
    Fig. 3.9. Design 3 CAD: early holder with S-curved arms and rail (top left), split cup on a rack and pinion (bottom left), refined holder (right).
  </figcaption>
</figure>

<figure markdown>
  ![One cycle of the single-cup holder](../images/design/d3-single-cycle.jpg){ width="1000" }

  <figcaption>
    Fig. 3.10. One cycle of the single-cup holder (anatomy model).
  </figcaption>
</figure>

### 3.3.2 Multiple Cups

A single cup harvests one head per cycle. The multi-cup version places four cups on one rack, each with its own pair of S-rails, closed together by one pinion, with one jet line under all four stems (Fig. 3.11). One actuator and one jet now serve a whole row, recovering the row-at-a-time throughput of Design 1 without its loose handling.

<figure markdown>
  ![One cycle of the multi-cup holder](../images/design/d3-multi-cycle.jpg){ width="1000" }

  <figcaption>
    Fig. 3.11. One cycle of the multi-cup holder (anatomy model).
  </figcaption>
</figure>

## 3.4 Final Design: Harvester_v2

The final design builds the multi-cup holder into a station over the conveyor (Fig. 3.12). Its key parameters are listed in Table 3.5, and one cycle from the SolidWorks motion study is shown in Fig. 3.13.

<figure markdown>
  ![Harvester_v2 in SolidWorks](../images/design/final-solidworks.jpg){ width="1000" }

  <figcaption>
    Fig. 3.12. Harvester_v2 in SolidWorks: station over the conveyor (top left), half-cups between S-curved tines (top right), heads in the holders (bottom left) and cut head tipped onto the tray (bottom right).
  </figcaption>
</figure>

<div markdown style="text-align: center;">
**Table 3.5.** Key parameters of Harvester_v2 (from the CAD model).
</div>

| Parameter | Value |
|---|---|
| Holders per row | Three half-cup pairs at 300 mm pitch, matching the row pitch of the CAD tray model |
| Drive | One gearmotor pinion between two opposed racks, so both halves close symmetrically |
| Cup | Revolved funnel: about 21–26 mm inner diameter at the stem, 111–116 mm at the rim |
| Cup travel | Open 64 mm per side; entry 22 mm per side (44 mm gap); closed |
| Leaf guide | S-curved tine rail rising from 40 mm to 114 mm above the tray |
| Cut | One waterjet sweeping 22 mm upward through the stem zone below the cups |
| Release | Cups open; each head tips forward about 65° onto the tray beside its stub |
| Indexing | Conveyor advances 300 mm per row |
| Simulated cycle | About 8 s per row of three |

<figure markdown>
  ![One cycle of Harvester_v2](../images/design/final-cycle.jpg){ width="900" }

  <figcaption>
    Fig. 3.13. One cycle of Harvester_v2 from the SolidWorks motion study.
  </figcaption>
</figure>

In each cycle:

1. The tray indexes the next row in while the cups are half-closed.
2. The S-rails lift the leaves, and the stems slide into the 44 mm entry gap.
3. The racks close the cups.
4. The jet cuts the stems.
5. The cups open, and each head tips forward onto the tray with its roots exposed.
6. The row moves on.

The motion study was checked frame by frame so that no part passes through another, and the tipped head comes to rest about 0.5 mm above the tray. The head never leaves the tray's support, so there is no drop into a chute.

!!! note "Throughput"
    At about 8 s per row of three, the simulated rate is 3 × 3,600 ÷ 8 ≈ 1,350 heads per hour. That is about 13–18 times the observed manual rate of 75–100 heads per hour, within the team's target of 10–40 times. The cycle time is a motion-study assumption that must be confirmed on hardware.

!!! note "Closing force"
    Because one pinion drives both racks, the closing force is set by motor torque: F = T / r. With a pitch radius of 10 mm and three cups per rack, limiting each cup to a force F<sub>c</sub> requires T = 3 F<sub>c</sub> r. For an illustrative F<sub>c</sub> of 2 N this is only 0.06 N·m. Crop safety therefore depends on limiting motor current, not on motor size. The safe value of F<sub>c</sub> is unknown and will be found by test.

## 3.5 Summary of Design Iterations

<div markdown style="text-align: center;">
**Table 3.6.** How each design answered the weakness of the one before.
</div>

| Design | What it fixed | What it left open |
|---|---|---|
| 1: Fork lift + flip | Clears a whole row at once without grippers | Lift actuator; loose heads; comb sticking; drop into chute and bin |
| 2: Two-axis gantry | No flip, no comb; heads stay level | Two coordinated motors; heads still loose; still a drop |
| 3: Single cup | Head gathered and held gently through the cut | One head per cycle |
| 3: Multi-cup | A row per cycle with one drive and one jet | Release path; even closing; jet sizing |
| Final: Harvester_v2 | Opposed racks on one pinion; heads stay on the tray, no drop | Jet pressure, cup force and release still to be tested |

## 3.6 Waterjet Stem Cutting

### 3.6.1 Evidence for a Waterjet Cut

In 2013, UC Davis and Fresh Express ran two trials comparing knife cutting with waterjet cutting of salad-cut romaine. Lettuce was cut into 2-inch pieces, bagged in air and stored at 2.5 °C for up to 20 days, then scored for visual quality, discoloration and whitening of the cut edges [20]. At 18 days, the sharp-nozzle waterjet was the best treatment, and in the second trial the sharp-nozzle waterjet was clearly better than both knives by 12 days (Fig. 3.14). The published study confirms that romaine cut with a food-grade waterjet nozzle kept better cut-surface quality than blade-cut romaine when stored without a modified atmosphere [21].

<figure markdown>
  ![Blade-cut and waterjet-cut romaine](../images/design/ucdavis-blade-vs-waterjet.jpg){ width="550" }

  <figcaption>
    Fig. 3.14. Blade-cut and waterjet-cut romaine after 8 and 18 days of storage (UC Davis and Fresh Express trials [20]).
  </figcaption>
</figure>

The trials used an industrial waterjet pump at 35,000–55,000 psi (about 2,400–3,800 bar). The pressure washers considered below reach 100–145 bar, so the trial results cannot be assumed for this design without testing.

### 3.6.2 Pressure Washer Comparison

Four off-the-shelf pressure washers were compared as the water supply for the jet (Table 3.7).

<div markdown style="text-align: center;">
**Table 3.7.** Pressure washer comparison. Specifications from manufacturer or retailer pages [16]–[19]; prices from the team's survey.
</div>

| Specification | Makita HW102 | Makita HW1300 | Kärcher K5 | Sun Joe SPX3000 |
|---|---|---|---|---|
| Price (team survey) | $200 | $600 | $880 | US$200 |
| Max pressure | 100 bar (1,450 psi) | 130 bar (1,885 psi) | 145 bar (2,103 psi) | 140 bar (2,030 psi) |
| Flow | 6 L/min | 7.5 L/min | 8.3 L/min | 6.7 L/min |
| Motor | 1,300 W universal | 1,800 W universal | 2,100 W, water-cooled | 1,800 W universal |
| Self-priming (draws water from a tank) | Not stated | Yes | Yes | Not stated |
| Adjustable pressure | No | Yes | Yes | No |

### 3.6.3 Jet Calculations

These figures assume each washer runs at its maximum pressure and maximum flow at the same time, with no losses in the hose or nozzle and one nozzle taking the whole flow. Pressure P is in pascals (1 bar = 100,000 Pa), flow Q is in m³/s (1 L/min = 1/60,000 m³/s) and water density ρ is 1000 kg/m³.

- **Jet velocity:** v = √(2P / ρ)
- **Hydraulic power:** P × Q
- **Equivalent nozzle diameter:** d = √(4Q / (π × v))
- **Jet force on the target:** F = ρ × Q × v

**Worked example**, Makita HW102 (100 bar, 6 L/min):

- v = √(2 × 10,000,000 ÷ 1000) ≈ 141 m/s
- Hydraulic power = 10,000,000 Pa × 0.0001 m³/s = 1,000 W
- Nozzle diameter = √(4 × 0.0001 ÷ (π × 141)) ≈ 0.95 mm
- Jet force = 1000 × 0.0001 × 141 ≈ 14 N

Applying the same relations to all four washers gives the results in Table 3.8. The equivalent stress is the jet force spread over a 10 mm stem (78.5 mm²), following the impact model used by the previous cohort [22], whose design stress is 0.30 MPa (a tissue failure stress of 0.20 MPa × a safety factor of 1.5).

<div markdown style="text-align: center;">
**Table 3.8.** Ideal jet properties for each washer (team calculation).
</div>

| Washer | Rating | Jet velocity | Hydraulic power | Nozzle diameter | Jet force | Stress on 10 mm stem |
|---|---|---|---|---|---|---|
| Makita HW102 | 100 bar, 6.0 L/min | 141 m/s | 1,000 W | 0.95 mm | 14.1 N | 0.18 MPa |
| Makita HW1300 | 130 bar, 7.5 L/min | 161 m/s | 1,625 W | 0.99 mm | 20.2 N | 0.26 MPa |
| Kärcher K5 | 145 bar, 8.3 L/min | 170 m/s | 2,014 W | 1.02 mm | 23.7 N | 0.30 MPa |
| Sun Joe SPX3000 | 140 bar, 6.7 L/min | 167 m/s | 1,554 W | 0.92 mm | 18.6 N | 0.24 MPa |

The previous cohort estimated, with this impact-stress model, that a 0.5 mm nozzle needs about 74 MPa to sever a 10 mm stem [22]. That is 7.4 times the HW102's 10 MPa. On the same model, the HW102's full 14 N spread over a 10 mm stem gives 0.18 MPa, below the 0.30 MPa design stress, and sharing the flow among three stems lowers it further.

Commercial waterjet harvesters do cut whole romaine in the field [23], so the model is probably conservative: a jet cuts by eroding a narrow kerf rather than loading the whole cross-section. Pressure, nozzle size and stand-off must therefore be found by test before a pump is chosen.

!!! warning "Still to be tested"
    All results in this section come from CAD, anatomy models, motion studies and calculation. Jet pressure, safe cup closing force, and damage when the heads tip onto the tray will be tested on hardware in Semester 2.
