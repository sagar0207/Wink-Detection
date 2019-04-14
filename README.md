# Wink-Detection
This project deals with different images for wink detection.

It contains two programs:
1.	A simple program that can detect a winking face.
Approach: Program uses two Haar cascades available in OpenCV. For face detection, haarcascade_frontalface_alt2.xml is used and haarcascade_eye.xml is used for eye detection. Provided the image folder that contains input images as command line argument, program calls the function called run_on_folder(face_cascade, eye_cascade, folderName), where face_cascade and eye_cascade are the haar cascades used in the program. This function will resize the image and detect all the faces in the images and for each face detected it will call another function called detect(img, faceCascade, eyeCascade) to detect whether the face is winking face or not. Here, program after detecting the face, will divide the face into two part left and right and individually use eye cascade on both the part to detect an eye.

2.	A program by applying filters on image detect a winking face.
Approach: First, Histogram equalization and medianBlur filter are applied on the image. Then, it uses the same approach as program 1.

