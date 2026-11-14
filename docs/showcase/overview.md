# System Overview

Harvester_v2 is a harvesting station that sits over ArianeTech's existing tray conveyor. It holds each lettuce head by the base of its stem in a split cup, cuts the stem with a waterjet, and sets the head back down on the tray, so the leaves are never gripped and nothing drops into a chute.

## How it works

1. The conveyor indexes the next row of lettuce in, 300 mm at a time.
2. S-curved rails lift the outer leaves, and the stems slide into the open cups.
3. One gearmotor drives two opposed racks, closing all three cups together around the stems.
4. A single waterjet sweeps under the cups and cuts the stems.
5. The cups open and each head tips forward onto the tray, leaving the root stub behind.

## Key figures

| | |
|---|---|
| Heads per row | 3, at 300 mm pitch |
| Simulated cycle | About 8 s per row |
| Simulated rate | About 1,350 heads per hour, 13–18 times the manual rate |
| Cut | One waterjet below the cups; no blades touch the crop |

For the full design development, see [3. Design Development](../report/design.md#36-harvester_v2-automated-lettuce-harvester-without-lift).

## Design 1 in motion

Harvester_v2 grew out of Design 1, the fork-lift harvester. In Design 1 the conveyor carries the lettuce to a fork on a lift unit inside the blue frame, a fixed waterjet cuts the stems, and the heads are stripped down a chute into a collection bin. Its problems with loose heads and the drop into the bin led to the later designs ([Section 3.3](../report/design.md#33-design-1-fork-lift-harvester)).

<figure>
  <video controls muted playsinline preload="metadata" style="width: 100%; max-width: 1000px;">
    <source src="../../videos/design-1-motion-study.mp4" type="video/mp4">
    Your browser cannot play this video.
    <a href="../../videos/design-1-motion-study.mp4">Download the motion study video</a>.
  </video>
  <figcaption>
    SolidWorks motion study of Design 1: conveyor, lift unit in the blue frame, discharge chute and collection bin.
  </figcaption>
</figure>
