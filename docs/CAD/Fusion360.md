---
title: Fusion360 - Bits & Bobs
---

Fusion 360
> Random bits which can help.

<!-- @IGNORE:MORFOLOGIK_RULE_EN_GB@ -->
And some notes here, just, avoid mesh editing stuff in Fusion, it does NOT like it very much, especially slightly messy meshes, I had an assembly I downloaded from thingiverse which was all compound meshes - which is fine if I wanted to print it as-is, but of course, I did not. So I had to mesh-edit, Fusion seems to handle bigger mesh sets like that a little crappily compared to, say, Blender. Obviously expected, Blender specialises in meshes.

Still, made me go a little nutty waiting for it to finish the mesh ops.

## Check a face, to see if it's a curve
<pre>SOLID > Inspect > Measure</pre>
If the face shows a Radius/Diameter then it's a curve, flat faces will NOT show a curve radius or diameter.