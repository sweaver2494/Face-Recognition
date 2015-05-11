README

Used in this project:

Windows 7 64-bit
MS Visual Studio 2013
OpenCV v. 2.4.11


Install OpenCV from here:
http://sourceforge.net/projects/opencvlibrary/files/opencv-win/

Documentation for Face Recognitin with OpenCV:
http://docs.opencv.org/modules/contrib/doc/facerec/facerec_tutorial.html#face-database

Guides on installing and configuring OpenCV on Windows:
https://www.youtube.com/watch?v=e_TQ9c3n_d8
http://opencv-srf.blogspot.com/2013/05/installing-configuring-opencv-with-vs.html


Files/Folders:

VS2013: Contains visual studio files to run the program.
	Face_Recogntion.cpp: main file to run webcam and perform face recognition.

	Different recognition models can be created.
	Ptr<FaceRecognizer> model = 
		createFisherFaceRecognizer(); //Fisher Faces
		createEigenFaceRecognizer(); //Eigenvector Faces (PCA)
		createLBPHFaceRecognizer(); //Local Binary Patterns Histograms

	The xml data files for cascade predictions are in the OpenCV files.

Python: Auxiliary scripts
	crop_face.py: Crops faces of pictures of people, which will be used as the training data.
	create_csv.py: Creates a csv file of all cropped photos, which is used as input for Face_Recognizer.cpp.