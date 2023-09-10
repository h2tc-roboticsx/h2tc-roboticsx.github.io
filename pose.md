---
title:  Pose
# feature_image: "/assets/images/throw-catch.png"
excerpt: 
---

#### &#x2022; Human Pose&Shape Extractor
[tbd: add code and guideline]
Our [pose extractor tool](https://github.com/lipengroboticsx/H2TC_code/blob/Tools) provides 2d&3d human pose and shape extraction. 
Note we did not capture the whole-body human pose directly.
Accurate whole-body tracking typically requires subjects to
wear a tight mocap suit, which would pose constraints to
human activities, particularly during dynamic manipulation.
<br>
Hence, we design an optimization algorithm to recover the 2d&3d human performance. 
We first detect 2d human poses via Openpose. 
These 2d poses, combined with the recorded RGBD and optitrack information, are then taken into consideration as observations to direct the 3D pose and shape extraction. In particular, we use the differentiable human model SMPLH to aid in robust fitting. The extraction results are like this:  
<table  >
 <tr>
<td  >
<img src="https://raw.githubusercontent.com/lipengroboticsx/lipengroboticsx.github.io/lx_test/assets/images/pose_extractor.png" width=1000>
</td>
</tr>
</table  > 
<!-- <img src="https://raw.githubusercontent.com/lipengroboticsx/lipengroboticsx.github.io/lx_test/assets/images/pose_extractor.png" width=1000> -->
