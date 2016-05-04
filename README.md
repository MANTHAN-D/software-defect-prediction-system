# cmpe239-project

Software Defect Prediction System

Team Dexter

Developers:
	Chirag Sejpal
	Rushil Shah
	Manthan Doshi

READMe

Software Defect Prediction System is a CK metric based defect prediction model that uses K-means clustering and Ant Colony Optimization algorithm 
to perform data mining on the logs of various defect tracking tools.

Set-up instructions

The system consists of two components.

1. Front-End

	a. Set ip address of machine to 10.0.0.203
	b. Set-up MongoDB server. Create a database named "cmpe239"
	c. Unzip the "front-end.zip" from Source-code in desired location.
	d. cd to unzipped front-end directory and start the nodejs server.	
	
2. Back-End
	https://github.com/MANTHAN-D/software-defect-prediction-server

Note: If both the systems are to be executed on same machine, do following and compile the back-end to generate .war file:
	Back-end:
		-- Change line 36 of file project_dir/src/main/java/dao/ModellingDataDAO.java to following:
			private static final String RESOURCEBASEURL = "http://localhost:3000/clusters/getData?source=";
			
	Front-end:
		-- Change line 76 of file project_dir/routes/upload.js to following:
			url: 'http://localhost:8080/software-defect-classification-service/rest/classificationService/classify'

Bibliography:

1. http://openscience.us/repo/defect/ck/ (Datasets)
