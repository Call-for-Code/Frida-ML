# Frida-ML

Frida, AI and IoT comes to the aid of teachers, students, and first responders. A Call for Code project from IBM.

As artificial intelligence and machine learning have taken mobile app development by storm, we are aiming to apply AI and ML into Frida e2e solution to increase user's satisfaction and provide intelligent capabilities during preparing, during and after natural disaster. In addition, we build the deep learning process by using Watson Studio and make AI and ML easily accessible by application developers. 

## 1. Predict earthquake's mangnitude

Earthquake detection and location has been studied and researched for many years by seismologists. In our solution, we leveraged the latest algorithm [ConNetQuake](http://advances.sciencemag.org/content/4/2/e1700578) which is highly scalable convolutional neural network for earthquake detection and location from a single waveform. We have improved the alogrighm and reduced Deep learning layers. 

**Data**: 
The training data is obtained from Oklahoma (USA). [IRIS data](https://www.iris.edu/hq/)

**Training env**:
Use 'GPU enabled Jupyter Notebook' in Watson Studio (current in closed beta) to train DL model. 
The Training data ('GSOK029_8-2016.mseed') with 34K records of data is loaded into Cloud Object Storage which is created in WS's project as following ![waveform](https://github.com/IBM/Frida/blob/master/docs/images/Waveform.png)

## 2. Recognize classroom damage patterns

In order to determine scape route and set right rescue priority, we will train `Visual Recognition Model` in Watson Studio and get saved Classroom damaged level's model endpoint. 
The following steps are to Train Watson Visual Recognition Without Code in [Watson Studio](https://www.ibm.com/ca-en/marketplace/watson-studio):
1. [**Sign up**](https://dataplatform.cloud.ibm.com/registration/stepone?context=wdp&apps=all) in IBM Watson Studio
2. **Create a New project**, From the Projects page in Watson Studio, add a new project.
When prompted, select the Visual Recognition project type.
If you have no instances of the Visual Recognition service, a new instance will be created. If you have existing instances, you have a choice:
Click the Existing option to associate an existing instance with the project
Click the New option to create another new instance
3. **Prepare your images**: Collect a minimum of 10 images (damaged classroom and normal classroom) for each class in .zip files, and then upload them to your project.
4. **Add .zip files** to your model from the data panel. (If the data panel isn't open, you can open it by clicking the Find and add data icon)
5. **Click Train Model**.
6. **Test your custom model**: in the Test area of the Visual Recognition model builder:
Test individual image files by dragging them from your computer onto the test area.
7. **Use trained VR model in your application**:
 -  **API key**
You can find your API key in the Visual Recognition service credentials:
Select "Watson Services" from the Services drop-down list in Watson Studio. This shows all your Visual Recognition service instances.
Click the Visual Recognition service instance you want to use.
View the credentials in the Credentials tab, and then copy the API key.
 -  **Model ID**
After creating a custom model in Watson Studio, you can find the model ID for your custom model in the Visual Recognition model builder:
From the Assets page of your project, click a Visual Recognition custom model to open that model in the model builder. In the Overview area of the model builder, you can find the model ID.
-  **Sample code**
After creating a custom model in Watson Studio, you can find sample code for using your custom model in the Visual Recognition model builder:
From the Assets page of your project, click a Visual Recognition custom model to open that model in the model builder. In the Implementation area of the model builder, you can find sample code.

If you would like to have detail instruction, please refer to [VR in Watson Studio ](https://www.ibm.com/support/knowledgecenter/DSXDOC/analyze-data/visual-recognition-overview.html)
