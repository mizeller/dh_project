# About
This repository consists of a forked version of [EasyMocap](https://github.com/zju3dv/EasyMocap) with the goal to establish a pipeline that features the combination of 3D reconstruction of static scenes and capuring human motion in the same scene. For the 3D reconstruction, [Nerfstudio](https://github.com/nerfstudio-project/nerfstudio) is used. 

# Installation
## 1. Installing Nerfstudio
To install nerfstudio, follow the instruction in the [installation guidelines](https://github.com/nerfstudio-project/nerfstudio0/blob/main/docs/quickstart/installation.md#dependencies).
## 2. Installing OpenPose
Follow the installation guide from [OpenPose](https://github.com/CMU-Perceptual-Computing-Lab/openpose).
## 3. Installing EasyMocap
```bash
conda create --name easymocap -y python=3.9
conda activate easymocap
python -m pip install --upgrade pip
```
```bash
git clone
cd 
```
# Demo
Extract frames for pose estimation from 3D reconstruction and extrinsic videos.
```bash
python preprocessing.py --reconstruction-video path.. --cam-left path... --cam-right...

```
Use [COLMAP](https://github.com/colmap/colmap) to determine camera extrinsic and instrinsic parameters.
```bash
conda activate nerfstudio
ns-process-data images --data path... --output-dir path... 

```
Use Nerfstudio to reconstruct 3D scene and export point-cloud.
```bash
ns-train nerfacto --data path
ns-export point-cloud --data path.. --output-dir 

```
Use OpenOse to detect 2D keypoints.
```bash
command

```
Use EasyMocap to generate 3D keypoints and SMPL body model.
```bash
command

```
