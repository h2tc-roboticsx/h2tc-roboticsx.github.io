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


Learning and imitating behavioral intelligence from human demonstrations is a promising approach towards the intuitive programming of robots for enhanced dynamic dexterity. However, there has been no publicly available dataset in this domain. To address this gap, we introduce the first large-scale dataset and recording framework specifically designed for studying human collaborative dynamic dexterity in throw&catch tasks. The dataset, named **H<sup>2</sup>TC**, contains 15,000 multi-view and multi-modal synchronized recordings of diverse **H**uman-**H**uman **T**hrow&**C**atch activities. It currently includes 34 healthy human subjects and a variety of 52 objects commonly manipulated in human throw&catch tasks. The dataset is accompanied by a hierarchy of manually annotated semantic and dense labels, such as ground truth human hand and object motions, making it well-suited for a wide range of robot studies, including low-level motor skill learning and high-level action recognition. We envision that the proposed dataset and recording framework will facilitate learning pipelines to extract insights on how humans coordinate both intra- and interpersonally to throw and catch objects, ultimately leading to the development of more capable and collaborative robots. 

<!-- The dataset has been well processed and stored in [Dropbox](https://www.dropbox.com/home/H2TC/), ensuring high quality and usability. Additionally, we have developed a suite of utility [tools](https://h2tc-roboticsx.github.io/tools/) to support the processing, visualization, and easy usage of the dataset. All resources can be found on the project [webpage](https://h2tc-roboticsx.github.io/index) and GitHub code [repository](https://github.com/h2tc-roboticsx/H2TC/). -->


#### About the Webpage 
<!-- Project Webpage: [Insert project webpage link here] GitHub Repository: [Insert GitHub repository link here] -->

On this project webpage, as well as the accompanying GitHub [repository](https://github.com/h2tc-roboticsx/H2TC/), you will find comprehensive documentation, tutorials, and examples to help you understand the [dataset](https://h2tc-roboticsx.github.io/dataset/) effectively. It also introduces a suite of utility [tools](https://h2tc-roboticsx.github.io/tools/) that have been designed to assist you in preprocessing, visualization, and analyzing the dataset.  The webpage also provides information on the data [collection](https://h2tc-roboticsx.github.io/recorder/) process, preprocessing steps, and data structure, making it easy for you to get started with the dataset. 

<!-- The GitHub [repository](https://github.com/h2tc-roboticsx/H2TC/) contains all the code and resources required to use the utility tools. These tools have been designed to assist you in preprocessing, visualizing, and analyzing the dataset. The repository also includes sample code to demonstrate the usage of these tools. -->

The dataset has been well processed and stored in [Dropbox](https://h2tc-roboticsx.github.io/notpubyet/), ensuring high quality and usability. All the code and resources required to use the dataset have been saved in the GitHub [repository](https://github.com/h2tc-roboticsx/H2TC/). Please feel free to explore the resources provided and let us know if you have any questions or need further assistance. 
<!-- We are committed to ensuring that you have a seamless experience working with our dataset and tools. -->



#### The Dataset in Numbers

Some facts about our dataset:

<table  width=1200>
    <tr  width=120>
        <td  bgcolor="#eeeeee">Subjects</td>
        <td  bgcolor="#eeeeee">34 subjects (29 males, 5 females, 20-31 yrs) </td>
    </tr>
    <tr>
        <td  >Objects</td>
        <td   >52 objects (21 rigid objects, 16 soft objects, 15 3D-printed objects)</td>
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
@article{lipeng2023h2tc,
  title={Advancing Robots with Greater Dynamic Dexterity: A Large-Scale Multi-View and Multi-Modal Dataset of Human-Human Throw&Catch of Arbitrary Objects},
  author={Lipeng, Chen* and Jianing, Qiu* and Lin, Li* and Xi Luo and Guoyi, Chi and Yu, Zheng},
  journal={arXiv},
  year={2023}
}
```




