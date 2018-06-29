## Object Detection using CNTK and Faster-RCNN

### Pre-requisites
* VC++ Redistributable is installed 
* If you are using GPU for training, Check if your card is  CUDA supported 
(https://www.geforce.com/hardware/technology/cuda/supported-gpus )
* Install the latest CUDA drivers  if not already installed 
( https://developer.nvidia.com/rdp/cudnn-download )
* Open CV ( for lower versions of CNTK ) 
( CNTK 2.2 requires OpenSource Computer Vision (OpenCV) to be installed, but it is optional for CNTK 2.3+.  )

### Setting up CNTK- python environment 
3 types of installation
* Python only  (https://docs.microsoft.com/en-us/cognitive-toolkit/setup-test-python ) 
* Script driven 
* Manual 
or 
* Docker setup   (https://docs.microsoft.com/en-us/cognitive-toolkit/cntk-docker-containers )
- Docker setup to support GPU needs installation of NVDIA-Docker ( which is currently not supported in windows )

_We will do the “python only” set up_

CNTK versions supported  - 
* CPU 
* GPU
_We will set up for the GPU version_

### Versions at the end 
This will be the versions of the packages that we will be ending up installing/ configuring 
* conda 4.2.9
* python 3.5
* cntk 2.5.1
* keras 2.2.0
* Model : AlexNet
* Imageset : Grocery

## Step 1 - Setting up the CNTK-python environment
Assumption : anaconda is pre-installed.
Create a new anaconda environment
```
conda create -n cntkpy35 python=3.5
activate cntkpy35
pip install cntk-gpu

```
Note : There were some DLL compatability(from CUDA libraries) with python versions 3.4 and 3.6 , hence we are using python 3.5

<< IMAGE COMES HERE>>

## Check for the versions 
In the conda environment
```
python
import cntk;
print (cntk.__version__)
>> 2.5.1
```

### Install  the supporting libraries and keras
```
pip install opencv-python easydict pyyaml
pip install  keras
```
## Check if keras is using CNTK as backend 
```
set KERAS_BACKEND=cntk

python
import keras;

```
This should show that CNTK is being used in the backend

<< IMAGE COMES HERE >>

### Getting the sample files 
In the conda environment , go to the working directory
get the samples files from github

```
python -m cntk.sample_installer 
```






