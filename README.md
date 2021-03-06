# A-EYE: Mobile Application for Visually Impaired People.

### Overview
A-EYE is a Flutter based mobile application. This application helps the visulaly impaired people to visualise and navigate through their surroundings. All they have to do is to launch the app using Google's TalkBack feature, and then onwards, the app will take care of the rest. Once, the user in inside the app, the app warmly invites the user and gives them the choice of Object Detection or OCR. 
- In the Object Detection module, the user will just have to point the mobile's camera to the world, and the app will start detecting objects in real-time. 
- In the OCR, the user just has to point the mobile's camera at a price tag of a product. After that, the app will tell the user about the price, expiry date, etc of that product.


The app uses deep learning for object detection provides the name of the object and its position relative to the user (either left side or right side) as an audio output. It also uses Optical Character Recognition to scan text and provide the price and expiry date of the product.    

- Flutter framework was used to develop this application, thus, this app will run on Android as well as on iOS platforms.  
- TensorFlow Lite and MobileNet provide the necessary dependencies and will do the required object detection.    

#### SYSTEM BLOCK DIAGRAM:  
<img src="images/block_diagram.png" width="400" alt="my image">

### Modules:  
##### Module 1:  User Interface  
Android/iOS application is built using Flutter Framework and Google TalkBack utilisation. Flutter supports Dart Language. Hence User Interface is created in Dart Language. UI consist of Home Page which cordially invites blind users to start the app through audio. There are two options provided for users:    
1) Start Object Detection!  
2) OCR  
  
##### Module 2:  Object Detection  
Given an image or a video stream, the object detection model can identify which of the known sets of objects might be present in the surroundings and provide information about their positions within the image. An object detection model is trained to detect the presence and location of multiple classes of objects. When we subsequently provide an image to the model, it will output a list of the objects it detects, the location of the bounding box that contains each object, and a score that indicates the confidence that detection was correct.
For each detected object, the model will return an array of four numbers representing a bounding rectangle that surrounds its position. For the starters, the model will return the numbers in the order as follows:[top,left,right,bottom].
Object with maximum accuracy is labelled and its speech output is given.
Pretrained model : MobileNet  
  
##### Module 3:  OCR  
OCR module is used to convert the text inside the image into an actual text. Our app needs this to recognise the content on the price tags, etc and to extract important information like the product name, contents and price tags. 
To do this we have divided the photo into two halves. The lower half is generally where the price is. This saves extra computations. Further in the lower half, we then focus on the text which is bold or which has a bigger text size than the rest of the text inside the image.  
  
##### Some sample images of the applications :      
<img src="images/homepage.png" height="300" alt="my image">      <img src="images/object_detection.png" height="300" alt="my image">      <img src="images/ocr.png" height="300" alt="my image">  


### Thank you! ☺️












