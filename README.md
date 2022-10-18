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
