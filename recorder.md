---
title:  Recorder
# feature_image: "/assets/images/throw-catch.png"
# permalink: /recorder
excerpt: 
---

Our recording framework consists of a variety of high-precision
motion track and visual streaming systems, which are
bundled with a suite of ancillary [devices](#device-details), [tools](https://github.com/h2tc-roboticsx/H2TC/tree/main/src/tools) and
[customized scripts](https://github.com/h2tc-roboticsx/H2TC/tree/main/src). The framework supports high-quality
synchronized streaming, saving and visualization of human
throw&catch activities from multiple sensors with varying
sampling rates and data formats. 

If you aim to record your human demonstrations like ours, we provide step-by-step [instructions](https://github.com/h2tc-roboticsx/H2TC/tree/main#recorder) and [scripts](https://github.com/h2tc-roboticsx/H2TC/blob/main/src/recorder.py) in the GitHub [repository](https://github.com/h2tc-roboticsx/H2TC/) of the dataset. 


<div align="center">
<img src="https://raw.githubusercontent.com/h2tc-roboticsx/H2TC/main/doc/resources/hardware.png" width=1600>
</div>


### Device Details
<!-- <table >
    <tr>
        <td  width=100>Device</td>
        <td  width=350> Manufacturer </td>
        <td  width=350> Recording Content </td>
        <td   width=350> FPS </td>
        <td   width=350> Resolution </td>
    </tr>
    <tr>
        <td  >① Gloves</td>
        <td ><a href=https://stretchsense.com/> StretchSense MoCap Pro</a> </td>
        <td  > Primary's Hand Pose </td>
        <td  > 120 </td>
        <td  > - </td>
    </tr>
    <tr>
        <td  >① Gloves</td>
        <td ><a href=https://stretchsense.com/> StretchSense MoCap Pro</a> </td>
        <td  > Primary's Hand Pose </td>
        <td  > 120 </td>
        <td  > - </td>
    </tr>
</table  > -->

Our recording framework employs multiple motion track and visual streaming systems, whose specifications are shown briefly below.
We refer users to our [paper](toadd) for a quick overview of how they are deployed and to their official product pages for detailed technical specifications. 


| Device | Manufacturer | Recording Content |FPS |Resolution  |
|:-----|:-----:|:-----:|:-----:|:-----:|
| ① Gloves | [StretchSense MoCap Pro](https://stretchsense.com/) | Primary's Hand Pose | 120 | - |
| ②⑤ Tracker | [OptiTrack](https://optitrack.com/) |  6D Head Pose | 240 | - |
| ③ Event Camera | [Prophesee](https://www.prophesee.ai/) | Event | - | 1280x720 |
| ④ ZED Camera | [Stereolabs](https://www.stereolabs.com/zed-2/) |  RGB-D | 60 | 1280x720 |

<br>


We apply Precision Time Protocol (PTP) to synchronize their clocks with a precision of sub-milliseconds (**around 0.3 ms**). The maximum offset across data streams is ≤ 1 frame at 60 FPS, as evaluated during manual annotation.  We refer users to the provided technical [document](https://github.com/h2tc-roboticsx/H2TC/blob/main/doc/processing_techdetails.md) in the GitHub [repository](https://github.com/h2tc-roboticsx/H2TC/), which explains in detail how we process and synchronize each data modality.




<!-- | ⑥⑦ Human Skeleton | [Stereolabs](https://www.stereolabs.com/zed-2/) |  RGB-D | - | 1280x720 | -->


<!-- #### Manual Guide

Our recorder integrates the functionality of arranging the content to be recorded, recording with multiple devices, and annotating the result of the recording into one user-friendly interactive program. 

**First**, enable all recording devices and ensure each of them function smoothly. Three ZED cameras and one Prophesee event camera should be wired to the host where the recorder program is supposed to run. StretchSense MoCap Pro gloves should be wireless connected to a Windows machine with its official client software Hand Engine running. OptiTrack server can be either operated on a separate host, recommended by us, or on the same host as any of the two aforementioned ones a.l.a. the computational resource allows and the performance will not be thus compromised. You may need to configure the firewall on each machine to allow the smooth (UDP) communication among them.

**Second**, update the configuration in our OptiTrack NatNet client code and rebuild the NatNet client. You need to set the values of OptiTrack server IP address (TODO Variable Name), recorder IP address (TODO Variable Name), and recorder port (TODO Variable Name) according to your network setting in the file `/recording/Optitrack_NatNet_client/src/example_main.cpp`.  TODO rebuild instruction

```p

```

**Third**, initialize your lists of subjects and objects in the corresponding files `/register/subjects.csv` and `/register/objects.csv` respectively. Each subject and object should lie in a new line. Please check the sample lists in our repository for detailed format.

**Next**, launch the main recorder application:

```

```

and the NatNet client:

```

```

now you should be able to see the prompt indicating that these two applications have successfully communicated with each other, if everything goes well, as shown blow 

TODO pictures of connection established.

**Last**, operate the main recorder to record following the interactive instruction. The main recorder will automatically communicate with and command Hand Engine and NatNet client to record. Nevertheless, we do recommend you to regularly check Hand Engine and NatNet client to see if bug.

TODO picture of a complete take -->
