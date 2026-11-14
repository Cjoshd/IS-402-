# 2. Concept Development and Selection

## 2.1 Systematic Ideation

The design process began with a brainstorming exercise conducted using Miro, an online collaborative whiteboard. The team identified challenges associated with harvesting leafy green vegetables and proposed a range of unconventional solutions using virtual sticky notes. These ideas were deliberately exaggerated or impractical to encourage creative thinking without being constrained by technical feasibility during the initial ideation stage.

<figure markdown>
  ![Miro Board Ideation](../images/miro.png){ width="1100" }

  <figcaption>
    Fig. 2.1. Miro Board Ideation
  </figcaption>
</figure>


From the identified harvesting challenges, five promising yet unconventional ideas were shortlisted for further development. Each idea was paired with a specific harvesting problem and arranged according to its degree of unconventionality.

The shortlisted ideas underwent an iterative refinement process involving five approaches: pivoting the original concept, reducing its complexity, incorporating existing technologies, improving ease of adoption by farms, and simplifying operation. Through this process, the initial ideas were progressively transformed into more practical mechanical solutions.

For example, the proposed use of water pistols to separate lettuce stems evolved into fixed waterjet nozzles, while an oversized fork intended to scoop entire lettuce heads was refined into smaller tines capable of sliding beneath the leaves to support the crop. Similarly, the idea of using an animal to reach elevated growing racks contributed to the development of a conveyor-based approach for positioning cultivation trays.


<figure markdown>
  ![Iterative refinement of unconventional ideas](../images/arrow.png){ width="1100" }

  <figcaption>
    Fig. 2.2. Iterative refinement of unconventional ideas
  </figcaption>
</figure>

These refined ideas formed the basis for subsequent concept generation, with several features incorporated into the proposed harvesting mechanisms.
## 2.2 Morphological Analysis

Following the initial ideation exercise, a morphological chart was developed to systematically explore alternative harvesting mechanisms. The overall harvesting operation was decomposed into five sub-functions:

1. Presenting the crop to the machine, 
2. Locating individual rows,
3. Separating the crop from the growing tray,
4. Lifting the harvested crop, and 
5. Releasing it from the mechanism.

For each sub-function, the team brainstormed and sketched multiple potential solutions. These included mechanisms adapted from existing technologies as well as original concepts developed during the ideation process.

<figure markdown>
  ![Morphological Chart](../images/moprh1.png){ width="1000" }

  <figcaption>
    Fig. 2.3. Morphological Chart
  </figcaption>
</figure>


By combining different solutions across the sub-functions, four distinct harvesting concepts were developed:

1. **Concept A** — Fork-Lift Harvester: Uses mechanical tines to support and lift lettuce heads along a cultivation row.

2. **Concept B** — Robotic Pick-and-Place: Employs a robotic manipulator and end-effector to handle individual crops.

3. **Concept C** — Continuous Clamp Belt: Uses opposing moving belts to grip and transport harvested crops.

4. **Concept D** — Waterjet and Vacuum Entry: Combines waterjet cutting with vacuum-assisted crop handling.

<figure markdown>
  ![Four harvesting concepts generated from the morphological chart](../images/4concepts.png){ width="1000" }

  <figcaption>
    Fig. 2.4. Four harvesting concepts generated from the morphological chart
  </figcaption>
</figure>

These concepts were subsequently evaluated to identify the most suitable approach for further development.

## 2.3 Concept Evaluation and Selection

Following the morphological analysis, four harvesting concepts were evaluated using a weighted decision matrix to identify the most suitable design for further development. Each concept was assessed against six criteria: crop damage, throughput, cost and part count, reliability and control simplicity, hygiene, and compatibility with standard cultivation trays.

Greater weight was assigned to crop damage (25%), throughput (20%), and cost (20%), reflecting the importance of maintaining crop quality while achieving efficient and economically viable harvesting operations. The remaining criteria comprised reliability and control simplicity (15%), hygiene (10%), and tray compatibility (10%).

Each concept was rated on a scale of 1 to 5, with the individual scores multiplied by their respective criterion weights to obtain an overall weighted score.

The fork-lift harvester (Concept A) achieved the highest weighted score of 4.10 out of 5, followed by the continuous clamp belt (Concept C) at 3.25, robotic pick-and-place system (Concept B) at 2.90, and waterjet gantry (Concept D) at 2.80.

<figure markdown>
  ![(a) Concept evaluation criteria and weightings
  (b) Weighted scores of the four harvesting concepts](../images/weightage.png){ width="900" }

  <figcaption>
    Fig. 2.5. (a) Concept evaluation criteria and weightings, (b) Weighted scores of the four harvesting concepts.
  </figcaption>
</figure>

Concept A was selected as the preferred design due to its ability to support and harvest an entire row of leafy vegetables simultaneously without directly gripping the leaves. Its relatively simple mechanical arrangement also offered potential advantages in throughput, control complexity, and minimising crop damage.

The selected concept subsequently served as the foundation for further design refinement and integration with complementary harvesting mechanisms.


## 2.4 Final Concept Development

Although Concept A achieved the highest overall evaluation score, certain features from the other concepts were identified as beneficial for further development. In particular, the waterjet cutting mechanism from Concept D was incorporated into the selected fork-lift harvester to form a hybrid design.

The hybrid concept retains the fork-lifting mechanism to support the leafy vegetables from below, while incorporating fixed waterjet nozzles to separate the stems. Unlike Concept D, which proposed a moving waterjet gantry, the hybrid design eliminates the need for an additional gantry axis by positioning the cutting nozzles at fixed locations.



During subsequent design refinement, opposing cup-shaped grippers were introduced beneath the fork structure to provide additional stabilisation around the base of each vegetable. The cups are designed to approach the plant from opposite sides, providing a larger contact area while avoiding direct compression of the leaves.

To accommodate simultaneous row-based harvesting, the cup-shaped grippers are intended to operate through a shared actuation mechanism. This allows multiple gripping units to be synchronised using a common drive system, reducing the need for individual actuators.



The resulting design combines fork-based leaf support, cup-shaped crop stabilisation, and waterjet cutting within a coordinated harvesting system. The detailed design of these mechanisms is presented in Chapter 3.

## 2.5 Summary of Final Design

The refined harvesting system integrates a fork-lifting mechanism, opposing cup-shaped grippers, a waterjet cutting system, conveyor belt, comb strips, and gravity chute to facilitate simultaneous harvesting of leafy green vegetables along a cultivation row.

The proposed harvesting sequence begins with the conveyor belt positioning the cultivation tray relative to the harvesting mechanism. The fork tines are then positioned beneath the lettuce leaves to provide support, while the opposing cup-shaped grippers approach the base of each plant to stabilise the crop during harvesting.

Once the vegetables are secured, the fixed waterjet nozzles cut the stems to separate them from their growing trays. Following separation, the harvested vegetables are transferred from the supporting structure using comb strips and directed towards the collection area through a gravity chute. The sequence is repeated as subsequent rows are positioned for harvesting.

The cup-shaped grippers are designed to operate through a shared actuation mechanism, enabling multiple harvesting units to grip their respective crops simultaneously. This arrangement aims to reduce the number of independently controlled actuators while maintaining coordinated handling across a cultivation row.

By combining row-based leaf support, controlled crop stabilisation, and fixed waterjet cutting, the proposed system aims to improve harvesting efficiency while minimising mechanical damage to the vegetables. The detailed mechanical design, component specifications, and integration of these mechanisms are discussed in Chapter 3.