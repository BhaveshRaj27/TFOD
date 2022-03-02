# TFOD
Object detection model for person and car detection
I used Tensorflow object detection API to do object detection here.
This is th link for the API https://github.com/tensorflow/models.git


# Model Name -    Faster R-CNN ResNet50 V1  
# Link for model weights and pipeline-  
http://download.tensorflow.org/models/object_detection/tf2/20200711/faster_rcnn_resnet50_v1_640x640_coco17_tpu-8.tar.gz

# About the Model
The model is currently the best version of the tradition object detection method. It overcome the various problems which traditional object detection show such as:
1.	Traditional object detection is divided into multiple stage so end to end training is not possible.
2.	Saving extracted feature take lots of memory.
3.	Feature extraction take lots of time
4.	Each extracted feature will feed to prediction model independently which make model very slow. 
The Faster R-CNN ResNet V1 overcome all the above problems and make better prediction than traditional object detection

![](https://github.com/BhaveshRaj27/TFOD/blob/main/images/RCNN.png)
Basic structure of Faster RCNN. Instead of VGG I am using Resnet.

# Assumption
1.	Do not require real time analysis.
2.	Most of the images are of same resolution. (size of images will be almost same)
3.	Split data into test and train dataset into 1:9 ratio
4.  Fine grain analysis needed.

 Basic flow for detection
 ![](https://github.com/BhaveshRaj27/TFOD/blob/main/images/flow.png)
 
# Inference
The model provide the Final Loss=0.15396827   . The metrics use is Precision. The value of the precision is 0.592879. This tell  us that about 60 % True positive(correct prediction) in total True prediction done by model. The result can be much better if batch size can be increased (I used batch size as 4 due limited GPU memory I have).  Batch size 32 or 64 will be giving better result. RCNN model is has provided good results as its full filled most of the analysis point

# Recommendation
1.	Can use different model as per project requirement such as Yolo.
2.	Should be trained with more data for better results.
3.	Better machine (GPU) can be used to go with better version of same model I used.
4.	If time allow write code from scratch and train model from scratch. It will give more control over model.

