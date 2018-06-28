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






