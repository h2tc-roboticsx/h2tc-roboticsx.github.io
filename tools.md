---
title:  Tools
# feature_image: "/assets/images/throw-catch.png"
excerpt: 
---

<!-- #### Tools -->
<!-- and extract human pose from the processed data. -->
This page provides tools to record,  process,  annotate and reconstruct human motions from the dataset. 
All source codes and supporting documents have been published in our GitHub [repository](https://github.com/h2tc-roboticsx/H2TC/) with a detailed installation [guide](https://github.com/h2tc-roboticsx/H2TC/blob/main/README.md). 
Briefly, <br>
    (1) <a href="https://h2tc-roboticsx.github.io/recorder/">Recoder</a> provides instructions, codes and documents on how to build a recording framework that supports high-quality synchronized streaming, saving and visualization of human-human throw&catch activities with multiple sensors. 
    <br> 
    <!-- (2) <a href="https://lipengroboticsx.github.io/tools/#-data-processing">processor</a> -->
    (2) [Processor](#data-processing) converts the raw data captured with the proposed recording frameworks (particularly the sensors) into the processed data of commonly used formats and aligns all data of different modalities.  <br>
    <!-- (3) <a href="https://lipengroboticsx.github.io/tools/#-annotator">annotator</a>  -->
    (3) [Annotator](#annotator) provides an interactive interface that supports users to visually validate and annotate each recorded throw&catch activity with a hierarchy of semantic and dense labels. <br>
    <!-- <a href="https://lipengroboticsx.github.io/tools/#-human-poseshape-extractor">Human pose&shape extractor</a>  -->
    (4) [Human pose&shape extractor](#human-poseshape-extractor) reconstructs 2d&3d human pose and shape from the multi-modality visual streams (coming soon). <br>

#### Data Processing

The [processor](https://github.com/h2tc-roboticsx/H2TC/tree/main/src) synchronizes all data streams captured from different sensors and converts the raw data into the processed data in commonly used formats as listed below. 
All data, both raw and processed,  are stored with a bunch of supporting files and in a hierarchical manner. 
We refer users to the [data explanation](https://github.com/h2tc-roboticsx/H2TC/blob/main/doc/data_file_explanation.md) and our technical [paper](toadd), for a detailed technical introduction of the data hierarchy and the content of each involved data file.<br>

<table style="width: 100%; margin-left: 0%; margin-right: 0%;">
    <tr  bgcolor="#696969">
        <td rowspan="2"   ><b>Device</b></td>
        <td colspan="2"  ><b>Raw</b></td>
        <td colspan="2"  ><b>Processed</b></td>
    </tr>
    <tr bgcolor="#696969">
        <td style="text-align: left;" ><b>Data</b></td>
        <td  style="text-align: left;" ><b>File</b></td>
        <td style="text-align: left;" ><b>Data</b></td>
        <td style="text-align: left;"><b>File</b></td>
    </tr>
    <tr >
        <td style="text-align: left;" rowspan="3">ZED</td>
        <td style="text-align: left;" rowspan="3" >Left- and right-eye RGB videos</td>
        <td style="text-align: left;" rowspan="3">.SVO</td>
        <td style="text-align: left;">RGB images</td>
        <td style="text-align: left;">.PNG</td>
    </tr>
    <tr >
        <td style="text-align: left;">Depth maps (unnormalized)</td>
        <td style="text-align: left;">.NPY</td>
    </tr>
    <tr  >
        <td style="text-align: left;">Depth images (normalized)</td>
        <td style="text-align: left;">.PNG</td>
    </tr>
    <tr bgcolor="#eeeeee" >
        <td style="text-align: left;" rowspan="2">Event</td>
        <td   style="text-align: left;">Binary events in EVT3.0 format</td>
        <td  style="text-align: left;">.RAW</td>
        <td style="text-align: left;">Events (<span class="math display">x, y, p, t</span>)</td>
        <td  style="text-align: left;">.CSV</td>
    </tr>
    <tr bgcolor="#eeeeee">
        <td  style="text-align: left;">Sensor setting for recording</td>
        <td  style="text-align: left;">.BIAS</td>
        <td style="text-align: left;">Event images</td>
        <td  style="text-align: left;">.JPG</td>
    </tr>
    <tr >
        <td style="text-align: left;" rowspan="4">MoCap Pro</td>
        <td style="text-align: left;">Sensors&#39; reading and hand joint angles</td>
        <td style="text-align: left;">.CSV</td>
        <td style="text-align: left;" rowspan="4">Hand joint motion</td>
        <td style="text-align: left;" rowspan="4">.CSV</td>
    </tr>
    <tr  >
        <td style="text-align: left;" >Hand calibration parameters</td>
        <td style="text-align: left;" >.CAL</td>
    </tr>
    <tr  >
        <td style="text-align: left;">3D animation visualization</td>
        <td style="text-align: left;">.FBX</td>
    </tr>
    <tr >
        <td style="text-align: left;">Metadata of the recording</td>
        <td style="text-align: left;">.JSON</td>
    </tr>
    <tr bgcolor="#eeeeee">
        <td style="text-align: left;">OptiTrack</td>
        <td style="text-align: left;">Local and global transformatiom matrices</td>
        <td style="text-align: left;">.CSV</td>
        <td style="text-align: left;">Body motio in throw-catch frame</td>
        <td style="text-align: left;">.CSV</td>
    </tr>
</table>
<br>

We refer users to our GitHub repository for more detailed step-by-step [instructions](https://github.com/h2tc-roboticsx/H2TC/blob/main#data-processing) on how to process the data from scratch.  Briefly, users can follow three steps below to process the raw data:<br> 
<b>Step 1</b>: Fetch the Raw Data. You can access all recorded raw data from <a href="https://www.dropbox.com/sh/ahet936ypjs1582/AACNYG0sjf1XdVxuZVLVL4fFa?dl=0">Dropbox</a>. The raw data of each recorded throw&catch activity  is packed in a `.zip` file. <br>
<b>Step 2</b>: Extract the Raw Data. We provide a scripted data [extractor](https://github.com/h2tc-roboticsx/H2TC/blob/main/src/extract.py) to unzip the packed raw data and also organize all raw files in a suitable data hierarchy, as mentioned before.   <br>
```bash
python src/extract.py --srcpath raw_data_path --tarpath your_path
``` 
<!-- <p style="margin-left: 1em;"> -->
<small >`--srcpath` is where you download the packed raw data. `--tarpath` is the target path where you want to extract the raw data. </small><br>
<!-- </p> -->
<b>Step 3</b>: Process the Extracted Data. Once the data is extracted and organized appropriately,  run the <a href=https://github.com/h2tc-roboticsx/H2TC/blob/main/src/process.py>processor</a>:<br>

```bash
python src/process.py --datapath your_path/data
```
<!-- <p style="margin-left: 1em;"> -->
<small >`--datapath` is where your extracted data is located. </small><br>
<!-- </p> -->

We refer users to the [data processing](https://github.com/h2tc-roboticsx/H2TC/blob/main/doc/processing_techdetails.md) for full technical details on how we process the multi-modal and cross-device raw data, and to the [data file explanation](https://github.com/h2tc-roboticsx/H2TC/blob/main/doc/data_file_explanation.md) and our technical [paper]() for a detailed introduction of the data hierarchy and the content of each involved data file.

#### Annotator

The [annotator](https://github.com/h2tc-roboticsx/H2TC/tree/main/src) supports users to visually segment and annotate each recorded activity with a hierarchy of semantic and dense [annotations](https://h2tc-roboticsx.github.io/dataset/#-Annotation). Overall,  the annotator offers  (1) An interactive annotation interface. The interface displays all synchronized streams in an interactive window as shown below, which allows users to inspect and annotate each recording frame by frame. <br>
    (2) A bunch of annotation operations. Users can easily interact with the interface to label segmentation and annotations with the keyboard operations.  
    (3) An information panel. The annotation result is displayed in real-time in the information panel. Any modification to the annotation result will be immediately saved in the corresponding annotation file. <br>


<table  >
 <tr>
<td  >
<img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/annotation_tool.png" width=1000>
</td>
</tr>
</table  >

<br>

We refer users to the full [guide](https://github.com/h2tc-roboticsx/H2TC/blob/main#annotation) for a detailed explanation of the annotator and its usage, as well as the dataset annotation.


#### Human pose&shape extractor

(Coming soon ...)