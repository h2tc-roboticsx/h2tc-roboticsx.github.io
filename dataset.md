---
title:  Dataset
excerpt: 
---

<!-- #### License -->

This page provides details of our [dataset](#the-dataset-in-numbers) and the supporting sources for downloading,
 <!-- <a href ="https://www.dropbox.com/sh/ahet936ypjs1582/AACNYG0sjf1XdVxuZVLVL4fFa?dl=0"><img decoding="async" src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc.github.io/main/assets/images/buttons/download_small.png"  width=20></a> ,  -->
 such as [annotations](#annotation) and [object models](#objects). Additionally, we offer a selection of [sample cases](#sample-cases) that showcase the human-human throw&catch activities featured in the dataset.

<!-- Briefly, as shown below, our dataset consists of multi-view synchronized <u>RGB</u>, <u>depth</u> and <u>event</u> streams of each human-human throw&catch activity, along with a hierachy of <u>semantic and dense annoataion</u>, such as <u>human  hand (both joint and 6D pose)</u> and  <u>human body</u> motions.
Below is a glance at the recorded visual streams in our dataset.  -->

Briefly, our dataset comprises multi-view synchronized <u>RGB</u>, <u>depth</u> and <u>event</u> streams for each human-human throw&catch activity. It is accompanied by a hierarchy of <u>semantic and dense annotations</u>, such as human hand joints and body motions, as shown below.



<div class="container" style="width: 100%;">
    <div class="row">
        <div class="col-lg-16">
    		<video muted autoplay loop width="100%">
        		<source src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/videos/v_all.mp4" type="video/mp4">
    		</video>
        </div>
    </div>
</div>

<br>

<!-- The dataset is recorded in a flat lab area, which resembles the real throw&catch scenes with unstructured, cluttered and dynamic surroundings.  We refer users to our [paper](toadd) and the Github [repository](https://github.com/h2tc-roboticsx/H2TC/)  for full details of the dataset construction. -->





####  Dataset Construction

The dataset is recorded in a flat lab area that closely resembles real-world throw-and-catch scenarios, featuring unstructured, cluttered, and dynamic surroundings,  as illustrated schematically below. For comprehensive details on the dataset construction, we encourage users to refer to our [technical paper](https://h2tc-roboticsx.github.io/underreview/) and the associated GitHub [repository](https://github.com/h2tc-roboticsx/H2TC/).


<table  >
 <tr>
<td  >
<img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/schema.png" width=700>
</td>
</tr>
</table  >

<br>

In addition, our dataset also provides a hierarchy of semantic and dense [annotations](#annotation), e.g. the ground truth human hand, body and object motions captured with motion capture systems. 


#### The Dataset in Numbers
  
Some facts about our dataset:

<table  width=1200>
    <tr  width=120>
        <td  bgcolor="#eeeeee">Subjects</td>
        <td  bgcolor="#eeeeee">34 subjects (29 males, 5 females, 20-31 yrs) </td>
    </tr>
    <tr>
        <td  >Objects</td>
        <td   >52 objects (21 rigid objects, 16 soft objects, 15 3D printed objects)</td>
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

<!-- All captured data, both raw  and processed, are stored  in Dropbox <a href ="https://www.dropbox.com/sh/ahet936ypjs1582/AACNYG0sjf1XdVxuZVLVL4fFa?dl=0"><img decoding="async" src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/buttons/download_small.png"  width=20></a> with rich [annotaions](#annotation) and other supporting files.  They are organized  with a bunch of [supporting files](https://github.com/h2tc-roboticsx/H2TC/tree/main/doc), such as [object models](#objects), and  in a hierarchical  manner. We refer users to the [data guide](https://github.com/h2tc-roboticsx/H2TC/blob/main/doc/data_file_explanation.md) and our technical [ paper](#paper), to understand details of the data hierachy and each stored data file in our dataset.<br>

We also provide a suite of scripted [tools](https://h2tc-roboticsx.github.io/tools/#data-processing) to facilitate the usage, open maintenance and extension of our dataset. -->

All captured data, both raw and processed, are stored in Dropbox <a href="https://h2tc-roboticsx.github.io/notpubyet/"><img decoding="async" src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/buttons/download_small.png" width=20></a>, complete with rich [annotations](#annotation) and other supporting files. The data is organized in a hierarchical manner, accompanied by a variety of 
[supporting tutorials](https://github.com/h2tc-roboticsx/H2TC/tree/main/doc) and files, such as [object models](#objects). We encourage users to consult the [data guide](https://github.com/h2tc-roboticsx/H2TC/blob/main/doc/data_file_explanation.md) and our [technical paper](https://h2tc-roboticsx.github.io/underreview/) to understand the details of the data hierarchy and each stored data file in our dataset.

Additionally, we provide a collection of scripted [tools](https://h2tc-roboticsx.github.io/tools/#data-processing) to facilitate the usage, open maintenance, and extension of our dataset.


####  Sample Cases


To offer a quick overview of the dataset,   we provide several sample cases here, which are available in Dropbox <a href="https://www.dropbox.com/scl/fo/exb0vj76ei789w58bzhqv/h?rlkey=bpc5qr22gr3qgdd3ierf32fpd&dl=0"><img decoding="async" src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/buttons/download_small.png"  width=20></a>. 
These samples include the recorded streams (both raw and processed) of six throw&catch activities involved in our dataset, as well as their annotation files. The data is organized hierarchically, as described earlier.
   
<table   width=1000 style="border-collapse: collapse; border-spacing: 1; text-align: left;">
    <tr >
        <td  width=400>Preview		        </td>
        <td  width=150> Take ID </td>
        <!-- <td  width=150> Catch Subject ID </td> -->
        <td  width=150> Object </td> 
        <td  width=650 > Description </td>
        <!-- <td  width=50> Download </td> -->
    </tr>
    <tr bgcolor="#eeeeee">
        <td   style="text-align: left;"><img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/001045.gif" width=400> </td>
        <td  > 001045 </td>
        <!-- <td  > xx </td> -->
        <td  > Helmet </td> 
        <td  style="text-align: left;"> 
        The auxiliary (right) subject threw a <u>'helmet'</u> with the <u>'right'</u> hand from the hand location <u>('right', 'chest')</u> and the body location <u>(1.17, 3.28)</u>,
        and then the primary (left) subject <u>successfully</u> caught the helmet with the  <u>'both'</u> hands from the hand location <u>('middle', 'chest')</u> and the body location <u>(0.21, 1.14)</u>.
</td>
        <!-- <td  > <a href ="https://github.com/lipengroboticsx/Human_Catch_Throw_Transfer"><img decoding="async" src="https://raw.githubusercontent.com/lipengroboticsx/lipengroboticsx.github.io/lx_test/assets/images/buttons/download_small.png"  width=50></a> </td> -->
    </tr>
    <tr >
        <td  style="text-align: left;"><img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/002870.gif" width=400> </td>
        <td  > 002870 </td>
        <!-- <td  > xx </td> -->
        <td  > Magazine </td> 
        <td  style="text-align: left;">   The  primary (left) subject threw a <u>'magazine'</u> with the <u>'both'</u> hands from the hand location <u>('middle', 'overhand')</u> and the body location <u>(1.2, 1.05)</u>,
        and then theauxiliary (right) subject <u>successfully</u> caught the magazine with the <u>'both'</u> hands from the hand location <u>('middle', 'underhand')</u> and the body location <u>(1.54, 3.01)</u>. </td>
        <!-- <td  > <a href ="https://github.com/lipengroboticsx/Human_Catch_Throw_Transfer"><img decoding="async" src="https://raw.githubusercontent.com/lipengroboticsx/lipengroboticsx.github.io/lx_test/assets/images/buttons/download_small.png"  width=50></a> </td> -->
    </tr >
          <tr bgcolor="#eeeeee">
        <td   style="text-align: left;"><img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/004521.gif" width=400> </td>
         <td  > 004521 </td>
        <!--<td  > xx </td> -->
        <td  > Apple <br> (3D printed) </td> 
        <td  style="text-align: left;"> 
        The  primary (left) subject threw an <u>'apple'</u> with the <u>'right'</u> hand from the hand location <u>('middle', 'chest')</u> and the body location <u>(0.15, 1.77)</u>,
        and then theauxiliary (right) subject <u>successfully</u> caught the apple with the  <u>'both'</u> hands from the hand location of  <u>('middle', 'underhead')</u> and the body location <u>(1.71, 4.47)</u>.   </td>
        <!-- <td  > <a href ="https://github.com/lipengroboticsx/Human_Catch_Throw_Transfer"><img decoding="async" src="https://raw.githubusercontent.com/lipengroboticsx/lipengroboticsx.github.io/lx_test/assets/images/buttons/download_small.png"  width=50></a> </td> -->
    </tr>
    <tr>
        <td  style="text-align: left;" ><img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/005915.gif" width=400> </td>
         <td  > 005915 </td>
        <!--<td  > xx </td>-->
        <td  > Beverage can </td> 
        <td  style="text-align: left;"> 
        The auxiliary (right) subject threw a <u>'beverage can'</u> with the <u>'left'</u> hand from the hand location <u>('middle', 'chest')</u> and the body location <u>(1.13, 3.29)</u>,
        and then the primary (left) subject <u>successfully</u> caught the can with the  <u>'both'</u> hands from the hand location  <u>('middle', 'chest')</u> and the body location <u>(0.92, 1.14)</u>. </td>
        <!-- <td  > <a href ="https://github.com/lipengroboticsx/Human_Catch_Throw_Transfer"><img decoding="async" src="https://raw.githubusercontent.com/lipengroboticsx/lipengroboticsx.github.io/lx_test/assets/images/buttons/download_small.png"  width=50></a> </td> -->
    </tr>
    <tr bgcolor="#eeeeee">
        <td  style="text-align: left;" ><img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/005616.gif" width=400> </td>
         <td  > 005616 </td>
        <!--<td  > xx </td>-->
        <td  > Bottled water </td> 
        <td  style="text-align: left;"> 
        The auxiliary (right) subject threw a <u>'bottled water'</u> with the <u>'both'</u> hands from the hand location <u>('middle', 'overhead')</u> and the body location <u>(1.19,4.00)</u>,
        and then the primary (left) subject <u>successfully</u> caught the bottle with the <u>'both'</u> hands from the hand location <u>('middle', 'chest')</u> and the body location <u>(0.36, 0.81)</u>.</td>
        <!-- <td  > <a href ="https://github.com/lipengroboticsx/Human_Catch_Throw_Transfer"><img decoding="async" src="https://raw.githubusercontent.com/lipengroboticsx/lipengroboticsx.github.io/lx_test/assets/images/buttons/download_small.png"  width=50></a> </td> -->
    </tr>
    <tr>
        <td style="text-align: left;"  ><img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/008683.gif" width=400> </td>
         <td  > 008683 </td>
        <!--<td  > xx </td>-->
        <td  > Doll </td> 
        <td  style="text-align: left;"> 
       The  primary (left) subject threw an <u>'doll'</u> with the <u>'right'</u> hand from the hand location <u>('middle', 'chest')</u> and the body location <u>(0.12, 1.75)</u>,
        and then theauxiliary (right) subject <u>successfully</u> caught the doll with  the <u>'both'</u> hands from the hand location  <u>('middle', 'chest')</u> and the body location <u>(1.65, 4.56)</u>.    </td>
        <!-- <td  > <a href ="https://github.com/lipengroboticsx/Human_Catch_Throw_Transfer"><img decoding="async" src="https://raw.githubusercontent.com/lipengroboticsx/lipengroboticsx.github.io/lx_test/assets/images/buttons/download_small.png"  width=50></a> </td> -->
    </tr>
</table>

<br>

#### Annotation

Our dataset offers a hierarchy of semantic and dense annotations, making it suitable for a variety of research applications, ranging from low-level physical skill learning to high-level pattern recognition. You can download and examine the sample annotations from Dropbox <a href ="https://www.dropbox.com/scl/fo/pz8nlw22sv01ai29aqysc/h?rlkey=ca6m9uu8p3ljkw06su75n40ek&dl=0"><img decoding="async" src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/buttons/download_small.png"  width=20></a>.  

Briefly,  each throw&catch activity in our dataset is labeled with:
<p style="margin-left: 0em; ">
<b>1. Human-object interaction states</b>. As depicted below, each involved throw&catch activity is segmented into four phases, including <u>pre-throwing</u>, <u>object flying</u>, <u>catching</u> and <u>post-catching</u>, with three manually annotated moments including <u>throw</u>, <u>catch touch</u> and <u>catch stable</u>. <br>
</p>

<table  > <tr><td  >  <img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/seg_00.png" width=1600></td></tr></table  >

<p style="margin-left: 0em;">
<b>2. Human hand, body and object motions</b>.  The ground truth human hand joint motions, 6D body and object motions are recorded with high-precision <a href="https://h2tc-roboticsx.github.io/recorder/">motion capture systems</a>, e.g. OptiTrack and MoCap gloves. 
</p>

<p style="margin-left: 0em;">
<b>3. Other semantic and dense annotations</b>.The human subjects' behaviors are manually inspected and annotated with symbolic labels, including <u>grasp mode</u> and <u>hand locations</u> during throw&catc, as shown below. Moreover, the subjects' <u>exact standing locations</u> and the <u>average flying speed of the object</u> are automatically annotated as quantitative labels.<br>
</p>

<table  > <tr><td  >  <img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/instruction.png" width=600></td></tr></table  >
<br>


The comprehensive annotation hierarchy is outlined below:



<table width=2000 style="text-align: left;">
    <tr bgcolor="#696969"  style="text-align: left;">
        <td  width=300> Name </td>
        <td width=1200> Description</td>
        <td width=500>  Value</td>
        <td width=200>  Labeling Type</td>
    </tr>
    <tr    style="text-align: left;">
        <td style="text-align: left;">Object</td>
        <td style="text-align: left;">The thrown object</td>
        <td style="text-align: left;"><i>'object_id'</i></td>
        <td>automatic</td>
    </tr>
    <tr bgcolor="#eeeeee" style="text-align: left;">
        <td style="text-align: left;"><b>Throw</b></td>
        <td style="text-align: left;">The moment when the subject's hand(s) breaks with the thrown object during throwing</td>
        <td style="text-align: left;">UNIX timestamp</td>
        <td >manual</td>
    </tr>
    <tr  style="text-align: left;">
        <td style="text-align: left;">- Grasp mode </td>
        <td style="text-align: left;"> The subject's grasp mode to throw the object at the "throw" moment</td>
        <td style="text-align: left;">{<i>'left'</i>, <i>'right'</i>, <i>'both'</i> } </td>
        <td  >manual</td>
    </tr>
    <tr style="text-align: left;">
        <td style="text-align: left;">- Throw vertical</td>
        <td  style="text-align: left;">The vertical location(s) of the subject's  hand(s) to throw the object at the "throw" moment</td>
        <td style="text-align: left;">{<i>'overhead'</i>, <i>'overhand'</i>, <i>'chest'</i>, <i>'underhand'</i> } </td>
        <td >manual</td>
    </tr>
    <tr  style="text-align: left;">
        <td  style="text-align: left;">- Throw horizontal</td>
        <td  style="text-align: left;">The horizontal location(s) of the subject's  hand(s) to throw the object</td>
        <td  style="text-align: left;">{<i>'left'</i>, <i>'middle'</i>, <i>'right'</i> } </td>
        <td>manual</td>
    </tr>
    <tr  style="text-align: left;">
        <td  style="text-align: left;">- Catch vertical</td>
        <td  style="text-align: left;">The vertical location(s) of the subject's hand(s) to catch at the "throw" moment</td>
        <td  style="text-align: left;">{<i>'overhead'</i>, <i>'overhand'</i>, <i>'chest'</i>, <i>'underhand'</i> } </td>
        <td>manual</td>
    </tr>
    <tr  style="text-align: left;">
        <td  style="text-align: left;">- Catch horizontal</td>
        <td  style="text-align: left;">The horizontal location(s) of the subject's hand(s) to catch at the "throw" moment</td>
        <td  style="text-align: left;">{<i>'left'</i>, <i>'middle'</i>, <i>'right'</i> } </td>
        <td>manual</td>
    </tr >
    <tr  style="text-align: left;">
        <td  style="text-align: left;">- Throw location</td>
        <td  style="text-align: left;">The subject's exact body location to throw at the "throw" moment</td>
        <td  style="text-align: left;">(<i>x</i>, <i>z</i>)</td>
        <td>automatic</td>
    </tr>
    <tr  style="text-align: left;">
        <td  style="text-align: left;">- Catch location</td>
        <td  style="text-align: left;">The subject's exact  body location to catch at the "throw" moment</td>
        <td  style="text-align: left;">(<i>x</i>, <i>z</i>)</td>
        <td>automatic</td>
    </tr>
    <tr bgcolor="#eeeeee"  style="text-align: left;">
        <td  style="text-align: left;"><b>Catch_touch</b></td>
        <td  style="text-align: left;">The moment when the subject's hand(s) first touches the flying  object during catching</td>
        <td  style="text-align: left;">UNIX timestamp</td>
        <td>manual</td>
    </tr>
    <tr  style="text-align: left;" >
        <td  style="text-align: left;">- Catch location</td>
        <td  style="text-align: left;">The subject's exact location to catch the object at the "catch_touch" moment</td>
        <td  style="text-align: left;">(<i>x</i>, <i>z</i>)</td>
        <td>automatic</td>
    </tr>
    <tr  style="text-align: left;" >
        <td  style="text-align: left;">- Object speed</td>
        <td  style="text-align: left;">The  object's average speed during free flying</td>
        <td  style="text-align: left;">m/s</td>
        <td>automatic</td>
    </tr>
    <tr bgcolor="#eeeeee"  style="text-align: left;">
        <td  style="text-align: left;"><b>Catch_stable</b></td>
        <td  style="text-align: left;">The moment when the subject catches the flying object stably during catching</td>
        <td  style="text-align: left;">UNIX timestamp</td>
        <td>manual</td>
    </tr>
    <tr  style="text-align: left;">
        <td  style="text-align: left;">- Grasp mode</td>
        <td  style="text-align: left;">The subject's grasp mode to catch the object at the "catch_stable" moment</td>
        <td  style="text-align: left;">{<i>'left'</i>, <i>'right'</i>, <i>'both'</i> } </td>
        <td>manual</td>
    </tr>
    <tr  style="text-align: left;">
        <td  style="text-align: left;">- Vertical location</td>
        <td  style="text-align: left;">The vertical location(s) of the subject's hand(s) to catch the object at the "catch_stable" moment</td>
        <td  style="text-align: left;">{<i>'overhead'</i>, <i>'overhand'</i>, <i>'chest'</i>, <i>'underhand'</i> } </td>
        <td>manual</td>
    </tr>
    <tr  style="text-align: left;">
        <td style="text-align: left;">- Horizontal location</td>
        <td  style="text-align: left;">The horizontal location(s) of the subject's hand(s) to catch at the "catch_stable" moment</td>
        <td  style="text-align: left;">{<i>'left'</i>, <i>'middle'</i>, <i>'right'</i> } </td>
        <td>manual</td>
    </tr>
    <tr  style="text-align: left;">
        <td  style="text-align: left;">- Catch result</td>
        <td  style="text-align: left;">The result on whether the object is stably catched by the subject</td>
        <td  style="text-align: left;">{'<i>success</i>', '<i>fail</i>'} </td>
        <td>manual</td>
    </tr>
</table>
<br>

For additional information about the annotations, we encourage users to refer to our [technical paper](https://h2tc-roboticsx.github.io/underreview/) and the GitHub [repository](https://github.com/h2tc-roboticsx/H2TC/) of the dataset. Furthermore, we provide an [annotation tool](https://h2tc-roboticsx.github.io/tools/#annotator) accompanied by a comprehensive technical [tutorial](https://github.com/h2tc-roboticsx/H2TC/blob/main/README.md), enabling users to annotate custom-captured data from a recording framework similar to or identical to ours.
<br>

#### Objects

The dataset comprises a total of 52 objects, which can be broadly categorized into 21 rigid objects, 16 soft objects, and 15 3D-printed objects. These objects have been specifically selected as they are commonly found and manipulated in throw-and-catch activities within domestic and/or industrial settings. You can download the scanned object models from  Dropbox <a href ="https://www.dropbox.com/scl/fo/le7yd4zs4508nro6xw6mv/h?rlkey=8iegb7lu2po75c6uin25l8yxd&dl=0"><img decoding="async" src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/buttons/download_small.png"  width=20></a>.

<table >
    <tr>
        <td  width=450><img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/rigid_00.png" width=350></td>
        <td  width=450><img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/soft.png" width=350></td>
        <td  width=450><img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/3d_printed_00.png" width=350></td>
    </tr>
        <tr>
        <td > Rigid objects</td>
        <td > Soft objects  </td>
        <td > 3D printed objects </td>
    </tr>
</table>


<br> 


#### &#x2022; License
**All of our data is for academic use only. Any commercial use is prohibited!**
By downloading the data, you accept and agree to the terms of <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png" /></a><br />


<!-- <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>. -->
