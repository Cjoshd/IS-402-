# 2. Objective and Scope

## 2.1 Objective

The objective is to design and evaluate a harvesting module that separates whole lettuce heads from their roots at the end of ArianeTech's existing tray conveyor, faster than manual harvesting and without gripping the leaves. In Semester 1 the team:

1. analysed the manual workflow and located the bottleneck,
2. generated and selected concepts systematically, and
3. developed the selected concept through four design iterations, checked in CAD, anatomy animations and SolidWorks motion studies.

Semester 2 will build and test physical prototypes.

## 2.2 System Context and Project Scope

The module sits between the cultivation racks and packing. Its input is a tray of mature lettuce arriving on a conveyor; its output is a row of cut heads ready to be collected, with the root stubs left in the tray.

- **In scope:** presenting each row, holding the heads, cutting the stems and releasing the heads.
- **Out of scope:** retrieving trays from the racks, packing and tray washing.

Two interface rules come from the partner: the module must accept the farm's trays without modification, and unintended crop damage must be kept to a minimum [22].

## 2.3 Design Estimates

The harvesting mechanism must accommodate differences in lettuce size and weight while supporting the leaves gently during collection. Published measurements of hydroponic lettuce provided the initial design values, alongside observations made during the ArianeTech industry visit. These findings guided the working clearance, carrying capacity and contact arrangement summarised in Table 1.

<div markdown style="text-align: center;">
**Table 1:** Physical attributes of hydroponic lettuce and the design conclusions drawn from them.
</div>

| Attribute | Research-supported value | Design conclusion |
|---|---|---|
| Plant height | Height ranged from 161–212 mm, with a mean of 185.8 mm [13, Table 1]. | Provide adjustable height and sufficient clearance for the tallest plants in the intended crop. |
| Leaf droop | Observed during the ArianeTech industry visit. | Use a narrow insertion profile to reach beneath the leaves. Determine the insertion height through measurements of ArianeTech's lettuce. |
| Plant mass | Mass ranged from 113.23–196.36 g with roots and 102.45–179.67 g after root removal [13, Table 1]. | Adopt 230 g as the initial design payload and check carrying performance during lifting and transfer. |
| Extraction force from planting board | Extraction required 9.6–16.5 N, with a mean of 13.03 N [13, Sec. 3.3]. | Account for extraction resistance when sizing the lifting mechanism and secure the planting board against upward movement. |
| Leaf injury during gripping | Tested flexible-finger configurations recorded forces of approximately 1.67–2.33 N per finger and mean leaf injury areas of 120.3–275.5 mm² [10, Tables 3–4]. | Spread the contact load and limit squeezing of the leaves. Refine contact position and applied force through handling trials. |
| Moisture content | Average moisture content was 95.73% in leaves and 91.71% in stems [13, Table 2]. | Keep the transfer from harvesting to packing short. Check slipping and sticking on the selected contact material using lettuce in its actual harvesting condition. |
| Canopy diameter | Diameter ranged from 282–378 mm, with a mean of 331.6 mm [13, Table 1]. | Allow sufficient clearance around the canopy and set fork spacing according to the region supporting the plant. |

### Design requirements from lettuce

- **Load:** size carrying components for a 230 g payload, above the measured maximum of 196 g, and validate this allowance on ArianeTech's crop.
- **Contact:** flexible fingers applying about 2 N per finger still injured leaves [10]. Support the head without squeezing its leaves and refine contact force through testing.
- **Cut before lifting:** extraction requires 9.6–16.5 N [13], substantially exceeding the head's weight. The selected sequence cuts the stem before lifting to avoid this extraction load.
- **Edges:** round tine and cup edges to distribute contact loads and reduce snagging.
- **Size range:** accommodate heights of 161–212 mm and canopy diameters of 282–378 mm.

These requirements guide individual handling, while throughput determines overall capacity.

### Throughput target

The preliminary cost model targets 750–4,000 heads per hour, spanning 10 times the lower observed manual rate of 75 heads per hour to 40 times the upper rate of 100. The team will refine this target with ArianeTech.

## 2.4 Existing Solutions

Table 2 summarises the solutions reviewed, from laboratory grippers to commercial lines.

<div markdown style="text-align: center;">
**Table 2:** Existing harvesting solutions and why none fits the problem as posed.
</div>

| Solution | What it does | Limitation for this project |
|---|---|---|
| Soft-finger gripper [10] | Uses flexible fingers to grasp and lift hydroponic lettuce. | Leaf injury occurred at approximately 2 N per finger, highlighting the need to control contact force and position. |
| Twisted double-belt clamp [24] | Clamps and conveys rows of spinach, with reported harvesting success of 94% and damage of 3%. | Applies approximately 2.37 N of clamping force. Its suitability for delicate lettuce heads requires testing. |
| FingerVision robot [25] | Cuts lettuce on growing plates and transfers each head using a gripper with visual and tactile sensing. | Handles one head per cycle and relies on direct gripping, requiring assessment against the project's throughput and damage targets. |
| Hortiplan Harvest Automation [26] | Lifts plants out of gutters, then cuts. | Designed around gutters and would require adaptation to ArianeTech's trays. |
| Sormac CEA harvester [27] | Uses airflow to raise leaves for cutting by two circular knives, processing up to 80 gutters per hour. | Designed for harvesting leaves rather than supporting and transferring intact heads. Cutting blades serve multiple plants. |
| Ramsay Highlander [23] | Uses waterjets to cut six rows of field-grown romaine in one pass. | Designed for open-field harvesting and still relies on 12 workers to handle the cut heads. |
| Hamill tray harvester [15], [28] | Cuts microgreens grown in trays, with a reported cutting time of approximately three seconds per tray. | Whole lettuce heads need additional support after cutting to prevent toppling. |
| IS-404 [22] | Proposes tray separation, plant clamping and waterjet root detachment in the previous cohort's design. | The estimated waterjet pressure of 74 MPa and its performance on planted trays require experimental validation. |

The reviewed solutions highlight the importance of gentle support and clean cutting. Gripping can injure leaves, while field applications demonstrate waterjet cutting of whole lettuce. UC Davis trials also reported better cut-surface quality in waterjet-cut romaine than in blade-cut samples [21]. These findings guide the project towards supporting each head throughout cutting without squeezing its leaves. Combining this approach with ArianeTech's existing trays forms the focus of the proposed harvesting module.
