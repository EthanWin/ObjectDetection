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

```
pip install opencv-python easydict pyyaml future pillow
```

1.git clone https://github.com/bhrnjica/ObjectDetection
2. conda create -n new_environment python=3.5
conda activate new_environment
deactivate
activate new_environment
3. 
*install matplotlib
pip install matplotlib 
python -m pip install --upgrade pip
*install CNTK
pip install cntk
pip install easydict
pip install pyyaml
pip install opencv-python
pip install pillow

4.
switch path:
cd  C:\Users\”username”\Documents\GitHub\ObjectDetection\PretrainedModels
cd  C:\Users\ ethan.wu\Documents\GitHub\ObjectDetection\PretrainedModels
python  download_model.py 
5.
switch path:
cd ..
To train and evaluate a detector run
python Nokia3310_detection.py
fix hardcode
# detect objects in single image
img_path = os.path.join(os.path.dirname(os.path.abspath(__file__)), r"testImages/img30.jpg")


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
