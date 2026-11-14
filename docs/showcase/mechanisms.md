# Mechanism Design

Harvester_v2 was reached through four design iterations. Each one was built as an anatomy animation to watch a full harvesting cycle before any hardware was made, and each animation exposed a weakness that the next design fixed. The animations below follow that path in order. The full reasoning is in [3. Design Development](../report/design.md).

## Design 1: Fork-Lift Harvester

The conveyor brings a row of lettuce to a fork on a lift unit. The tines slide under the heads, a fixed waterjet cuts the stems, and the fork lifts and turns the row so a comb strips the heads down a chute into a collection bin.

<figure>
  <video controls muted playsinline preload="metadata" style="width: 100%; max-width: 1000px;">
    <source src="../../videos/design-1-anatomy.mp4" type="video/mp4">
    <a href="../../videos/design-1-anatomy.mp4">Download the video</a>.
  </video>
  <figcaption>Design 1 anatomy animation: conveyor, fork on the lift, chute and collection bin.</figcaption>
</figure>

The second animation shows the fork turning through 135° to tip the heads onto the comb and chute. A 135° turn sweeps less space than a full rotation, but the motor has to stop and reverse every cycle. Watching it also showed the main problems with Design 1: nothing holds the heads while the fork moves, and they land in a heap in the bin.

<figure>
  <video controls muted playsinline preload="metadata" style="width: 100%; max-width: 1000px;">
    <source src="../../videos/design-1-anatomy-135-flip.mp4" type="video/mp4">
    <a href="../../videos/design-1-anatomy-135-flip.mp4">Download the video</a>.
  </video>
  <figcaption>Design 1 anatomy animation with the 135° flip: heads tipped off the fork, down the chute and into the bin.</figcaption>
</figure>

## Design 2: Two-Axis Gantry

Design 2 removes the flip and the comb. A gantry over the end of the conveyor moves the fork on two axes: it slides under the front row, the jet cuts the stems, the vertical axis lifts the row level, and the horizontal axis carries it over the chute to release the heads. The heads stay level, but they still ride loose on the tines and still drop into the bin, and the machine now needs two coordinated motors and a bigger frame.

<figure>
  <video controls muted playsinline preload="metadata" style="width: 100%; max-width: 1000px;">
    <source src="../../videos/design-2-anatomy.mp4" type="video/mp4">
    <a href="../../videos/design-2-anatomy.mp4">Download the video</a>.
  </video>
  <figcaption>Design 2 anatomy animation: the fork lifts the row level and carries it over the chute.</figcaption>
</figure>

## Design 3: Single Cup Holder

Design 3 changes the question from "how do we lift the row?" to "what should hold each head while it is cut?". A split, funnel-shaped cup waits beneath the head, with an S-curved rail on each side. As the plant moves forward, the rails guide the outer leaves up and inward so the head enters the cup without being squeezed. A rack and pinion closes the two cup halves around the stem, and the jet cuts just below, leaving the roots behind while the head stays upright.

<figure>
  <video controls muted playsinline preload="metadata" style="width: 100%; max-width: 1000px;">
    <source src="../../videos/design-3-single-cup-anatomy.mp4" type="video/mp4">
    <a href="../../videos/design-3-single-cup-anatomy.mp4">Download the video</a>.
  </video>
  <figcaption>Single cup holder anatomy animation: S-curved rails, funnel cup and rack-and-pinion closing.</figcaption>
</figure>

## Design 3: Multiple Cup Holders

A single cup harvests only one head per cycle. The multi-cup version puts four cups on one shared rack, each with its own pair of S-curved rails. One pinion closes all the cups together and one waterjet line cuts under every stem, so a whole row is harvested per cycle while each head is still held on its own.

<figure>
  <video controls muted playsinline preload="metadata" style="width: 100%; max-width: 1000px;">
    <source src="../../videos/clamp.mp4" type="video/mp4">
    <a href="../../videos/clamp.mp4">Download the video</a>.
  </video>
  <figcaption>Multiple cup holders anatomy animation: four cups closed by one pinion, with one jet line under the row.</figcaption>
</figure>

## Final Design: Harvester_v2

The multi-cup holder was then built into a station over the conveyor, with three cups per row at 300 mm pitch. After the cut the cups open and each head tips forward onto the tray, so nothing drops into a chute. See the [System Overview](overview.md) for the final design animation.
