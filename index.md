---
title:  
# feature_image: "/assets/images/throw-catch.png"
excerpt: 
---

<div class="container" style="width: 100%;">
    <div class="row">
        <div class="col-lg-16">
    		<video muted autoplay loop width="100%">
        		<source src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/videos/home_imageshome_video.mp4" type="video/mp4">
    		</video>
        </div>
    </div>
</div>

<br>

#### Introduction


Learning and imitating behavioral intelligence from human demonstrations is a promising way towards the intuitive and efficient programming of robots for greater dynamic dexterity. However, there has been no dataset publicly available for this domain. To fill this gap, we introduce H<sup>2</sup>TC, the first large-scale dataset and recording framework with an emphasis on the human dynamic dexterity in throw&catch.  The dataset contains 15K  multi-view and multi-modal synchronized visual recordings of diverse **H**uman-**H**uman **T**hrow&**C**atch activities.  It includes for now 33 healthy human subjects and a variety of 52 objects commonly manipulated by throw&catch.
 The dataset is provided with a hierarchy of manually annotated
semantic and dense labels, e.g. the ground truth human and object motions, rendering it well suited for a wide range of
studies, e.g. low-level skill learning and high-level behavior recognition.  We envision that the proposed dataset and recording framework can facilitate learning pipelines to extract insights on how humans coordinate intra- and interpersonally to throw&catch   objects, and help lead to more capable and collaborative robots. 
 <!-- The [dataset](https://lipengroboticsx.github.io/dataset/) together with a suite  -->
<!-- of utility [tools](https://lipengroboticsx.github.io/tools/) is available.  -->


<br>

#### The Dataset in Numbers

Some facts about our dataset:

<table  width=1200>
    <tr  width=120>
        <td  bgcolor="#eeeeee">Subjects</td>
        <td  bgcolor="#eeeeee">34 subjects (29 males, 5 females, 20-31 yrs) </td>
    </tr>
    <tr>
        <td  >Objects</td>
        <td   >52 objects ( 21 rigid objects, 16 soft objects, 15 3D printed objects)</td>
    </tr>
    <tr>
        <td  bgcolor="#eeeeee" >Actions</td>
        <td  bgcolor="#eeeeee" >Every two humans perform 10 random actions (5 throwing actions, 5 catching actions)</td>
    </tr>
    <tr>
        <td   >Recordings</td>
        <td  >15K recordings </td>
    </tr>
    <tr>
        <td   bgcolor="#eeeeee">Visual Modality</td>
        <td   bgcolor="#eeeeee" >RGB, depth, event</td>
    </tr>
    <tr>
        <td    >View</td>
        <td    >Egocentric, static third-person (side), static third-person (back)</td>
    </tr>
    <tr>
        <td  bgcolor="#eeeeee">Annotations</td>
        <td  bgcolor="#eeeeee">Human hand and body motion, object motion, average object velocity, human  grasp mode, etc.</td>
    </tr>
</table>
<br>

#### Cite

If you use our Dataset, please consider citing

```
@article{
}
```




