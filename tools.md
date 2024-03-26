---
title:  Tools
# feature_image: "/assets/images/throw-catch.png"
excerpt: 
---

<!-- #### Tools -->
<!-- and extract human pose from the processed data. -->
This page offers tools for recording, processing, annotating, and reconstructing human motions from the dataset. All source codes and supporting documents are available in our GitHub [repository](https://github.com/h2tc-roboticsx/H2TC/), complete with a detailed [installation guide](https://github.com/h2tc-roboticsx/H2TC/blob/main/README.md). In summary: <br>
    (1) <a href="https://h2tc-roboticsx.github.io/recorder/">Recoder</a> provides instructions, codes, and documents on constructing a recording framework that supports high-quality synchronized streaming, saving, and visualization of human-human throw&catch activities using multiple sensors.
    <br> 
    <!-- (2) <a href="https://lipengroboticsx.github.io/tools/#-data-processing">processor</a> -->
    (2) [Processor](#data-processing) converts the raw data captured with the proposed recording framework (particularly the sensors) into processed data in commonly used formats and aligns all data across different modalities. <br>
    <!-- (3) <a href="https://lipengroboticsx.github.io/tools/#-annotator">annotator</a>  -->
    (3) [Annotator](#annotator) offers an interactive interface that enables users to visually validate and annotate each recorded throw&catch activity with a hierarchy of semantic and dense labels. <br>
    (4) [Human motion constructor](#Human-motion-construction-and-retarget) constructs and optimizes human motions using multi-modal data streams in the dataset, and re-target the constructed human motions to multiple robots and multi-fingered hands. <br>


#### Data Processing

The [processor](https://github.com/h2tc-roboticsx/H2TC/tree/main/src) synchronizes all data streams captured from different sensors and converts the raw data into processed data in commonly used formats, as listed below. 
All data, both raw and processed, are stored alongside a variety of supporting files and organized in a hierarchical manner. 
We refer users to [data processing tutorials](https://github.com/h2tc-roboticsx/H2TC/blob/main/doc/processing_tech_details.md) documentation,
 [data explanation](https://github.com/h2tc-roboticsx/H2TC/blob/main/doc/data_file_explanation.md) and our [technical paper](https://h2tc-roboticsx.github.io/underreview/) for a detailed introduction to the data hierarchy and the content of each involved data file.<br>

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
        <td style="text-align: left;" rowspan="3" >Left-eye and right-eye RGB videos</td>
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
        <td style="text-align: left;">Body motion in throw-catch frame</td>
        <td style="text-align: left;">.CSV</td>
    </tr>
</table>
<br>

We suggest users to visit our GitHub repository for more detailed, step-by-step [instructions](https://github.com/h2tc-roboticsx/H2TC/blob/main#data-processing) on processing the data from scratch. Briefly, users can follow the three steps below to process the raw data:<br> 

<b>Step 1</b>: Fetch the Raw Data. You can access all recorded raw data from [Dropbox](https://h2tc-roboticsx.github.io/notpubyet/). The raw data of each recorded throw&catch activity is compressed in a `.zip` file. <br>

<b>Step 2</b>: Extract the Raw Data. We provide a scripted data [extractor](https://github.com/h2tc-roboticsx/H2TC/blob/main/src/extract.py) to unzip the packaged raw data and organize all raw files in an appropriate data hierarchy, as previously mentioned.
```bash
python src/extract.py --srcpath raw_data_path --tarpath your_path
``` 
<small >`--srcpath` is where the downloaded raw data is stored. `--tarpath` is the target path where you want to extract the raw data. </small><br>

<b>Step 3</b>: Process the Extracted Data. After the data has been extracted and organized appropriately, run the [processor](https://github.com/h2tc-roboticsx/H2TC/blob/main/src/process.py) :
```bash
python src/process.py --datapath your_path/data
```
<small >`--datapath` is where your extracted data is located. </small><br>

We refer users to the [data processing](https://github.com/h2tc-roboticsx/H2TC/blob/main/doc/processing_tech_details.md) documentation for complete technical details on how we process the multi-modal and cross-device raw data. Additionally, take a look at the [data file explanation](https://github.com/h2tc-roboticsx/H2TC/blob/main/doc/data_file_explanation.md) and our [technical paper](https://h2tc-roboticsx.github.io/underreview/) for a detailed introduction to the data hierarchy and the content of each involved data file.

#### Annotator

The [annotator](https://github.com/h2tc-roboticsx/H2TC/tree/main/src) enables users to visually segment and annotate each recorded activity with a hierarchy of semantic and dense [annotations](https://h2tc-roboticsx.github.io/dataset/#-Annotation). Overall, it provides: <br>
(1) An interactive annotation interface: The interface displays all synchronized streams in an interactive window, as shown below, allowing users to inspect and annotate each recording frame by frame. <br>
(2) A variety of annotation operations: Users can easily interact with the interface to label temporal segmentation and annotations using keyboard operations. <br>
(3) An information panel: The annotation results are displayed in real-time in the information panel. Any modifications to the annotation results are immediately saved in the corresponding annotation file. <br>


<table  >
 <tr>
<td  >
<img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/images/annotation_tool.png" width=1000>
</td>
</tr>
</table  >

<br>

We recommend users to read the comprehensive [annotation guide](https://github.com/h2tc-roboticsx/H2TC/blob/main#annotation) for a detailed explanation of the annotator and its usage, as well as the dataset annotation.


#### Human Motion Construction and Retargeting 

<!-- ##### 1. Camera calibration
- The camera intrinsic matrix is:
```
[[693.91839599609375, 0.0, 665.73150634765625],
[0.0, 693.91839599609375, 376.775787353515625],
[0.0, 0.0, 1.0]]
```  
- The camera extrinsic matrix could be calculated by `annotator_camextr.py`. The `img_file` is the path of image to be annotated. As illustrated below, after annotating the ground corners `ABCD` (! be sure to follow the ABCD order), the camera extrinsic parameters (world to camera transformation) will be computed with Perspective-n-Point (PnP) algorithm. Camera intrinsic matrix `CamIntr.txt` and extrinsic matrix `CamExtr.txt` will be saved in `save_folder`. 
![cam_calib](./cam_calib.png) -->
  

##### Coarse human pose estimation

We use [mmhuman3d](https://github.com/open-mmlab/mmhuman3d/tree/main) to estimate the coarse human poses. <br>
1) Installation: please follow the [official getting started](https://github.com/open-mmlab/mmhuman3d/blob/main/docs/getting_started.md) for installation.   <br>
2) H2TC data: Download h2tc data and fetch the `rgbd0` image folder.  <br>
3) SMPL related resources and pretrained models: 
[SMPL](https://smpl.is.tue.mpg.de/) v1.0 and some other resources from [mmhuman3d](https://github.com/open-mmlab/mmhuman3d/tree/main) that are needed in this step.  <br>

   - [J_regressor_extra.npy](https://openmmlab-share.oss-cn-hangzhou.aliyuncs.com/mmhuman3d/models/J_regressor_extra.npy?versionId=CAEQHhiBgIDD6c3V6xciIGIwZDEzYWI5NTBlOTRkODU4OTE1M2Y4YTI0NTVlZGM1)
   - [J_regressor_h36m.npy](https://openmmlab-share.oss-cn-hangzhou.aliyuncs.com/mmhuman3d/models/J_regressor_h36m.npy?versionId=CAEQHhiBgIDE6c3V6xciIDdjYzE3MzQ4MmU4MzQyNmRiZDA5YTg2YTI5YWFkNjRi)
   - [smpl_mean_params.npz](https://openmmlab-share.oss-cn-hangzhou.aliyuncs.com/mmhuman3d/models/smpl_mean_params.npz?versionId=CAEQHhiBgICN6M3V6xciIDU1MzUzNjZjZGNiOTQ3OWJiZTJmNThiZmY4NmMxMTM4)
   - [Pretrained models](https://github.com/open-mmlab/mmhuman3d/blob/main/configs/spin/README.md) 

Download the resources and arrange them as follows:

```text
    mmhuman3d
    ├── mmhuman3d
    ├── docs
    ├── tests
    ├── tools
    ├── configs
    └── data
        ├── gmm_08.pkl
        ├── body_models
        │   ├── J_regressor_extra.npy
        │   ├── J_regressor_h36m.npy
        │   ├── smpl_mean_params.npz
        │   └── smpl
        │       ├── SMPL_FEMALE.pkl
        │       ├── SMPL_MALE.pkl
        │       └── SMPL_NEUTRAL.pkl
        ├── pretrained
        │   └── spin_pretrain.pth
        └── static_fits
            ├── coco_fits.npy
            ├── h36m_fits.npy
            ├── lspet_fits.npy
            ├── lsp_fits.npy
            ├── mpii_fits.npy
            └── mpi_inf_3dhp_fits.npy
```

To extract human poses from the input images or video with the human tracking and pose estimation, you can first `cd mmhuman3d` and then run:<br>

```bash
python demo/estimate_smpl.py configs/spin/resnet50_spin_pw3d.py data/checkpoints/spin_pretrained.pth --multi_person_demo --tracking_config demo/mmtracking_cfg/deepsort_faster-rcnn_fpn_4e_mot17-private-half.py --input_path L:/h2tc_dataset/002870/processed/rgbd0 --show_path vis_results/002870.mp4 --smooth_type savgol --speed_up_type deciwatch --draw_bbox --output vis_results/
```

The human poses are stored in folder `vis_results/inference_result.npz` with smpl format. <br>

##### Multi-modal based human pose optimization

1. Installation:<br>
```bash
conda create -n pose python=3.7
conda activate pose
conda install pytorch==1.6.0 torchvision==0.7.0 cudatoolkit=10.1 -c pytorch
pip install matplotlib, opencv-python,scikit-learn,trimesh,Pillow,pyrender,pyglet==1.5.15,tensorboard,git+https://github.com/nghorbani/configer,torchgeometry==0.1.2,smplx==0.1.28
```

2. Download [smplh](https://mano.is.tue.mpg.de/)<br>
3. File structure:
   
    ```text
    pose_reconstruction_frommm
    |--config.py
    |--fitting_utls.py
    |--h2tc_fit_dataset_mm.py
    |--motion_optimizer.py
    |--run_fitting_mm.py
    |--smplh_male.npz       # smplh model (male)
    |--fit_h2tc_mm.cfg      # config file
    ```

4. Run the multi-modal optimizer to to optimize the human poses with the opti-track data and glove hands. <br>

```bash
python pose_reconstruction_frommm/run_fitting_mm.py @./fit_h2tc_mm.cfg --data-path <h2tc_takeid_processed_folder> --mmhuman <mmhuman_file> --out <out_pose_folder>
```

 `<h2tc_takeid_processed_folder>`: the processed folder, like `root/002870/processed/rgbd0`. 

 `<mmhuman_file>`: the coarse pose file extracted from [Coarse human pose estimation](#2-coarse-human-pose-estimation), like `root/vis_results/inference_result.npz`

`<out_pose_folder>`: folder path to save the optimization pose results. The output meshes are saved in `<out_pose_folder>/body_meshes_humor`. Optimized human poses are saved in `<out_pose_folder>/results_out/stage2_results.npz` 

###### Optimization Algorithm

Due to inevitable visual occlusion, the results of [mmhuman](https://github.com/open-mmlab/mmhuman3d/tree/main) are coarse, especially in arms and hands. Taking into account the multi-modal data collected in our dataset, including OptiTrack, gloves poses, rgb images and so on, these information can help us optimize the [mmhuman](https://github.com/open-mmlab/mmhuman3d/tree/main) results. <br>   

Given the coarse [mmhuman](https://github.com/open-mmlab/mmhuman3d/tree/main) pose estimation $\mathcal{M_{mmh}}$, OptiTrack head and hands tracking points $\mathcal{H}$  and glove hands poses $\Theta_{hand}$, we aim to recover the accurate human poses $\mathcal{M_{acc}}$. Our optimization objective is: <br>

$$
\min _{\mathcal{M_{acc}} } \mathcal{C_{trk}} + \mathcal{C_{wst}} +\mathcal{C_{smo}}  
$$

The OptiTrack term $\mathcal{C_{trk}}$ measures how well the posed body model match the OptiTrack points 
$$\mathbf{P}_t = \left \{ \mathbf{d}_t^i \right \}_{i=0}^{3}$$ for head and two-hand points at each frame $t$. We use the mesh corresponding vertices 
$\mathbf{V}_t$ (index 411 for the head OptiTrack data, 5459 for the right hand and 2213 for the left hand) to compute <br>

$$
\mathcal{C_{trk}} =\lambda _{trk}\sum_{t=0}^{T}\sum_{i=0}^{3} \mathop{\min}_{\mathbf{v}_t^i}\left \| \mathbf{v}_t^i- \mathbf{d}_t^i \right \| ^2
$$

<!-- $\mathcal{C}_\text{trk} =\lambda _\text{trk}\sum_{t=0}^{T}\sum_{i=0}^{3}\omega_b  \mathop{\min}_{\mathbf{v}_t^i}\left \| \mathbf{v}_t^i- \mathbf{d}_t^i \right \| ^2$.  -->

<!-- $\omega_b$ is the robust bisquare weight based on the Chamfer distance.   -->

The wrist cost $\mathcal{C_{wst}}$ is used to disambiguate the right/left wrist pose guided by hands tracking information. Meanwhile, the cost also contributes to recovering accurate whole-arm poses even in severe occlusions. We use the hand OptiTrack pose $$\mathbf{O}_t^{hand} = \left \{ \mathbf{o}_t^h \right \}_{i=0}^1$$ to calculate the right $h=0$ and the left $h=1$ wrist loss. It is formulated as <br>

$$
\mathcal{C_{wri}} =\lambda _{wri}\sum_{t=0}^{T}\sum_{h=0}^{1}\left \| {\mathbf{v}_{wri}}_t^h-\mathbf{o}_t^h \right \| ^2 
$$

where ${\mathbf{v}_{wri}}_t^h$ is the SMPLH right/left wrist pose.  <br> 

Independent frame-by-frame pose estimation always causes temporally inconsistent. The regularization term $\mathcal{C_{smo}}$ is used to guarantee the smoothness of the motion recovering and keep it reasonable. The smooth term encourages the 3D joints consistency. It is formulated as <br>

$$
\mathcal{C_{smo}}= \sum_{t=1}^{T}
(\lambda_{jp}\sum_{j=1}^{N} \left \| \mathbf{J}_t^j - \mathbf{J}_{t-1}^j \right \|^2   
+\lambda_{bl}\sum_{i=1}^{B} ( l_t^i - l_{t-1}^i )^2
)
$$

$\mathbf{J}_t$ is the joint position at time $t$.
Bone lengths $l_t^j$ are from $\mathbf{J}_t^j$ at each step.  <br>

For hands pose, we already have captured the two hands poses $\Theta_{hand}$ in each capturing. We map them to SMPLH hands pose directly.  <br>

We initialize the optimization processing with the mmhuman poses. All $\lambda$ are weights to decide the contribution of each term.  <br>  

##### Retargeting

###### Smplh sequence pose -> General format animation (.fbx)

1. Installation: 

    a. Install [Python FBX](https://download.autodesk.com/us/fbx/20112/fbx_sdk_help/index.html?url=WS1a9193826455f5ff453265c9125faa23bbb5fe8.htm,topicNumber=d0e8312). 

    b. Open `SMPL-to-FBX-main` and `pip install -r requirements.txt`

2. SMPLX fbx: 
   
    Download the [SMPLX fbx model](https://smpl.is.tue.mpg.de) for unity Keep the female model `smplx-female.fbx` and male model `smplx-male.fbx`.

3. Here's the file structure:
   
    ```text
    SMPL-to-FBX-main
    |--Convert.py
    |--SMPLXObject.py
    |--FbxReadWriter.py
    |--<smplh_pose>/
    |  |--*.npz
    |--<fbx_path>/
    |  |--smplx-female.fbx
    |  |--smplx-male.fbx
    |--<output_path>/
    ```

4. Run 
   
```bash
    python Convert.py --input_motion_base <smplh_pose> --fbx_source_path <fbx_path>/smplx-female.fbx --output_base <output_path>
```

to start converting. The animation file will save in `<output_path>`. You can open it via Blender or Unity 3D.
   
##### Retargeting 

We use Unity 3D (2022.3.17) to demo the retargeting. Plese check the [tutorial video](https://www.youtube.com/watch?v=BEZHVYk6Fa4) first, then you can follow the steps:
<!-- 1. Model rigging: give an artist a mesh model, ask him to bound the mesh vertices to bones (it is called rigging in graphics) -->

1. Model rigging: given a mesh model, bound the mesh vertices to bones <br>
2. Specifying the corresponding skeleton joints between rigged model A and B: unity3d automatically solve it after setting the rigged models as `humanoid` in `animation type`.  <br>
3. Animation: please follow the above tutorial video. The animation algothrim used in Unity 3D is [Linear Blend Skinning (LBS)](https://zhuanlan.zhihu.com/p/78377681).  <br>

Four selected examples of motion construction and re-target are shown below: <br>

<table >
    <tr>
        <td > take one </td>
        <td > take two </td>
        <td > take three </td>
        <td > take four </td>
    </tr>
    <tr>
        <td  width=450><img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/motion_gif/1.gif" width=350></td>
        <td  width=450><img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/motion_gif/2.gif" width=350></td>
        <td  width=446><img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/motion_gif/3.gif" width=350></td>
        <td  width=450><img src="https://raw.githubusercontent.com/h2tc-roboticsx/h2tc-roboticsx.github.io/main/assets/motion_gif/4.gif" width=350></td>
    </tr>
</table>




