Object detection example using CNTK and Python
![Nokia3310](https://github.com/bhrnjica/ObjectDetection/blob/master/nokiasamplerecogn.png)

## Overview

This example is modified version of predefined CNTK Example of Image detection which can be found at http://github.com/Microsoft/CNTK.

By running `Nokia3310_detection.py` the code will do the following:

* Train and create CNTK based model whih can detect NOkia3310 on an image.
* By providing test images the model can be evaluated and tested.
* The example uses minimal python code, needed to run object detection by using FasterRCNN.
* The model is not trained from zero, it is based on AlexNet pre trained model.


## Running the example

### Setup

To run Nokia3310 object detection example you need a CNTK 2.5, Python 3.5 environment. In order to install CNTK2.5 you have to install Intel Math Kernel Library (MKLML) from this location https://github.com/intel/mkl-dnn/releases. Anyhow in order for proper installation of CNKT consult to the official site. 

Beside the basics requiremens you need to install the following additional packages:


1. 

c:\~\conda create -n new_environment python=3.5 pip
 
c:\~\conda activate new_environment
 
2.

c:\~\python -m pip install --upgrade pip

3.

c:\~\conda install git
 
4.

c:\~\git clone https://github.com/bhrnjica/ObjectDetection

5. 
#install matplotlib
 
 c:\~\pip install matplotlib


#install CNTK
 
c:\~\pip install cntk
 
```
c:\~\pip install opencv-python easydict pyyaml future pillow
```

4.
 #switch path:username depend on what's account you login.
 
 cd  C:\Users\”username”\~\ObjectDetection\PretrainedModels
 
 c:\~\python  download_model.py 

5.
 #switch path:
 
 C:\Users\”username”\~\ObjectDetection\PretrainedModels\cd ..
 
 #fix hardcode for type error 
 #edit Nokia3310_detection.py
 
 img_path = os.path.join(os.path.dirname(os.path.abspath(__file__)), r"testImages/img30.jpg")
 
 #To train and evaluate a detector run
 
 c:\~\python Nokia3310_detection.py
 
# detect objects in single image

#Change img30 for detect
#edit Nokia3310_detection.py

img_path = os.path.join(os.path.dirname(os.path.abspath(__file__)), r"testImages/img30.jpg")

#see the output folder 

->PATH:C:\~\ObjectDetection\FasterRCNN\Output\NO3310

###----------------------------------------------------------------------------------------------------------###
### Getting the data and AlexNet model

The example uses the pre-trained AlexNet model which can be downloaded by running the following Python command from the PretrainedModels folder:

`python download_model.py`

### Running the demo

To train and evaluate a detector run

`python Nokia3310_detection.py`

#### Changing the data set

In order to change DataSet you have to provide the images and data. More information about how to prepare image and data can be found at http://bhrnjica.net  


#### Changing the base model

Changing base model is not supported. 

addition package 
 c:\~\pip install easydict
 c:\~\pip install pyyaml
 c:\~\pip install opencv-python
 c:\~\pip install pillow
