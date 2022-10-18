# Face_Emotion_Recognition_Live_Stream
Emotion is a mental state associated with nervous system associated with feeling , perception,behavioral reactions and a degree of gratification or displeasure.Facial expressions are a form of nonverbal communication.One of the current application of artificial intelligence using neural networks is the recognition of faces in images and video for various applications.Face detection technology  can come in handy in various practical life examples.In this paper I have strived to represent a method for identifying seven emotions such as anger, disgust, fear, happy,surprise ,sad and neutral using deep learning  techniques.

![Alt text](https://edps.europa.eu/sites/default/files/styles/edps_wysiwyg_image/public/2021-05/facial-emotion-recognition-steps.png?itok=jYN0mnzI)

# Problem Statement
The Indian education landscape has been undergoing rapid changes for the past 10 years owing to the advancement of web-based learning services, specifically, eLearning platforms.Global E-learning is estimated to witness an 8X over the next 5 years to reach USD 2B in 2021. India is expected to grow with a CAGR of 44% crossing the 10M users mark in 2021. Although the market is growing on a rapid scale, there are major challenges associated with digital learning when compared with brick and mortar classrooms. One of many challenges is how to ensure quality learning for students.
Digital platforms might overpower physical classrooms in terms of content quality but when it comes to understanding whether students are able to grasp the content in a live class scenario is yet an open-end challenge.
In a physical classroom during a lecture the teacher can see the faces and assess the emotion of the class and tune their lecture accordingly, whether he is going fast or slow. He can identify students who need special attention. Digital classrooms are conducted via video telephony software program (exZoom) where it’s not possible for medium scale class (25-50) to see all students and assess the mood.Because of this drawback, students are not focusing on content due to lack of surveillance.While digital platforms have limitations in terms of physical surveillance but it comes with the power of data and machines which can work for you. It provides data in the form of video, audio, and texts which can be analyzed using deep learning algorithms. Deep learning backed system not only solve the surveillance issue, but it also removes the human bias from the system, and all information is no longer in the teacher’s brain rather translated in numbers that can be analyzed and tracked.

We will solve the above-mentioned challenge by applying deep learning algorithms to live video data. The solution to this problem is by recognizing facial emotions.

# Data Summary
The model is trained on the FER-2013 dataset downloaded from Kaggle.This dataset consists of 48x48 pixel grayscale images of faces. The training set consists of 28,709 images and the  test set consists of 7,178 images.The dataset consists of 7 different facial expressions as follows:

![Alt text](https://miro.medium.com/max/972/1*eslj3MRsR2fKAV3q1i3-5w.jpeg)

# Dependencies
* Python
* Tensorflow
* Keras
* OpenCV
* Pre Trained Haar Cascade
* Streamlit
* Streamlit-webrtc

# Model Creation
A Convolutional Neural Network, also known as CNN or ConvNet, is a class of neural network that specializes in processing data that has a grid-like topology, such as an image.A CNN typically has three layers: a convolutional layer, a pooling layer, and a fully connected layer.The layers are arranged in such a way so that they detect simpler patterns first (lines, curves, etc.) and more complex patterns (faces, objects, etc.) further along.The convolution layer is the core building block of the CNN. It carries the main portion of the network’s computational load.This layer performs a dot product between two matrices, where one matrix is the set of learnable parameters otherwise known as a kernel, and the other matrix is the restricted portion of the receptive field.The pooling layer replaces the output of the network at certain locations by deriving a summary statistic of the nearby outputs.Fully Connected Layers neurons in this layer have full connectivity with all neurons in the preceding and succeeding layer as seen in regular FCNN.

![Alt](https://raw.githubusercontent.com/travistangvh/emotion-detection-in-real-time/master/images/VGGFaceNetwork.jpg) 

# Loss and Accuracy Plot

A convolutional neural network can be evaluated using the ‘evaluate’ method. This method takes the test data as its parameters. Before this, the data is plotted on the console using ‘matplotlib’ library and ‘imshow’ methods.The accuracy versus epoch data is visualized.This is done using matplotlib library.The model is evaluated, and the loss and accuracy are determined.
![Alt](https://github.com/SampannaMishra/FaceEmotionRecognition/blob/main/visualization/finalval.JPG)

# Deployment of Streamlit Webapp on Cloud

Streamlit  which is an open source web framework has been used to build face emotion recognition web app.OpenCV, an open source computer vision and machine learning software library has also been used for real time face reading.The model weights were saved in json and h5 file format which were later used.Created a function FaceEmotion to detect multiple faces in video camera which further provides a bounding box around faces and predicts face emotion.
Streamlit library does not provide the live capture feature itself ,instead uses a third party API.
Therefore,I used streamlit-webrtc which helped to deal with real-time video streams. Image captured from the webcam is sent to the VideoTransformer function to detect the emotion.
Then this model was deployed on heroku platform. 

App link Deployed on Heroku is  (https://xcv-app.herokuapp.com/)

# Conclusion
* **The total epochs considered initially for the training the images was 45.Too many epochs can lead to overfitting of the training dataset, whereas too few may result in an underfit model. However by usage of early stopping which allowed  to specify an arbitrary number of training epochs and stop training once the model performance stops improving on a hold out validation dataset**.
* **The model created with CNN layers gave training accuracy 73.69% and validation accuracy 59.01% after 15 epochs**
* **The Fer2013 dataset used had less number of disgust images. So the model is unable to distinguish the disgust emotion.**

