
Follow to steps to create env ro run the project
(you need to have nvida GPU)

( ***********WARNING ISSUES CAN BE FACE IF Cuda Version are Different*********)

1) Download and install Anaconda and python (For this you are requred to have anaconda installed on your system)
	- if anaconda is not there then download and install it from this link: 'https://www.anaconda.com/products/distribution'

2) Create anaconda environment
	- Type 'anaconda prompt' in windows searchbox and open it.

	- Now type the following commands
		-- conda create -n project python==3.9.7
		-- conda activate project

	- Now go the project directory where requirements.txt file is there
		-- pip install -r requirements.txt
		-- jupyter notebook

	-  jupyter notebook will open the chrome browser (default)

3) Now open the yolov5.ipynb file
	-Run each cell by pressing SHIFT+ENTER

 	- Now in the cell where yolov5 model is loaded change the imagename.
	- Images for testing are provided in the test_images file.

4) Now run the code till the end of notebook after changing the image name.

5) Output Image will be seen in output_images folder.
	

************************************************************************
The Training file which is training.ipynb is more than 50mb. 
Thus it is not added in the submitted code.
 but Google Drive link is provided 

the link is: 