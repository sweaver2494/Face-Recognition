README

My System Specs:

Windows 7 64-bit
MS Visual Studio 2013
OpenCV v. 2.4.11


Install OpenCV from here:
http://sourceforge.net/projects/opencvlibrary/files/opencv-win/

Documentation for Face Recognitin with OpenCV:
http://docs.opencv.org/modules/contrib/doc/facerec/facerec_tutorial.html
http://docs.opencv.org/modules/contrib/doc/facerec/facerec_api.html

Guides on installing and configuring OpenCV on Windows:
https://www.youtube.com/watch?v=e_TQ9c3n_d8
http://opencv-srf.blogspot.com/2013/05/installing-configuring-opencv-with-vs.html


Files/Folders:

VS2013: Contains visual studio files to run the program.
	Face_Recogntion.cpp: Main file I created to interface with webcam and perform face recognition.

	Different recognition models can be created.
	Ptr<FaceRecognizer> model = 
		createFisherFaceRecognizer(); //FisherFaces
		createEigenFaceRecognizer(); //EigenFaces (PCA)
		createLBPHFaceRecognizer(); //Local Binary Patterns Histograms

	The xml data files for cascade predictions are located in the OpenCV library files.

Python: Auxiliary scripts
	crop_face.py: Crops faces of pictures of people, which will be used as the training data.
	create_csv.py: Creates a csv file of all cropped photos, which is used as input for Face_Recognizer.cpp.

Photos: Contains the original (uncropped) and cropped photos used in the training data set.
	Cropped: Each class has its individual sub-directory. For example, "Scott" is one class with multiple photos and "Reena" is another.
	photos_csv.ext: Ouput file created by create_csv.py. Contains path to each photo and its corresponding label.

OpenCV: Contains all .lib and .dll files referenced by Visual Studio.
	Since the library size is so large, I am not including it in the repository. It can be downloaded from here.
	Guides on installing and configuring OpenCV on Windows are here (YouTube video) and here (webpage tutorial).

