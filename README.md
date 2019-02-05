# Frida-ML

Frida, AI and IoT comes to the aid of teachers, students, and first responders. A Call for Code project from IBM.

As artificial intelligence and machine learning have taken mobile app development by storm, we are aiming to apply AI and ML into Frida e2e solution to increase user's satisfaction and provide intelligent capabilities during preparing, during and after natural disaster. In addition, we build the deep learning process by using Watson Studio and make AI and ML easily accessible by application developers. 

## 1.Predict earthquake's mangnitude

Earthquake detection and location has been studied and researched for many years by seismologists. In our solution, we leveraged the latest algorithm [ConNetQuake](http://advances.sciencemag.org/content/4/2/e1700578) which is highly scalable convolutional neural network for earthquake detection and location from a single waveform. We have improved the alogrighm and reduced Deep learning layers. 

**Data**: 
The training data is obtained from Oklahoma (USA). [IRIS data](https://www.iris.edu/hq/)

**Training env**:
Use 'GPU enabled Jupyter Notebook' in Watson Studio (current in closed beta) to train DL model. 
The Training data ('GSOK029_8-2016.mseed') with 34K records of data is loaded into Cloud Object Storage which is created in WS's project as following ![waveform](https://github.com/IBM/Frida/blob/master/docs/images/Waveform.png)



