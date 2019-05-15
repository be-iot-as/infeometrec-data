# Reconstructing Video from Interferometric Measurements of Time-Varying Sources . 
reconstructing video from infeometric measurment  of time varying sources .
“The Black Hole Image” Step by step .
Go to the profile of Taj Alagawani
Taj Alagawani
Apr 29
Imaging with the Event Horizon Telescope.

All of us had heard about capturing the first image of the black hole, in this story we will run the method used to create these images and videos.
We will use the technique Reconstructing Video from Interferometric Measurements of Time-Varying Sources . 
Let’s start working in Python 3 environment .

we will use EHT Imaging , you can get it from . Here .

ehtim (eht-imaging)
Python modules for simulating and manipulating VLBI data and producing images with regularized maximum likelihood methods.

The package contains several primary classes for loading, simulating, and manipulating VLBI data. The main classes are the Image, Array, Obsdata, Imager, and Caltable classes, which provide tools for loading images and data, producing simulated data from realistic u-v tracks, calibrating, inspecting, and plotting data, and producing images from data sets in various polariazations using various data terms and regularizers.



# Installation
change to the main directory and run:

pip3 install .
It should install most of the required libraries in your PY(env) by pip3 . or pip if use another version . 
(astropy, ephem, future, h5py , html , networkx, numpy, pandas , matplotlib, requests, scipy, skimage).

# Note : you can not use conda or any pkg manager to install ehtim , This version is an early release .

Now Exploring the VLBI Imaging Website : Here .
Standardized dataset of real & synthetic data , Over 5000 synthetic measurement sets: 14 Array Configurations, 96 Source Images, 4 Noise Levels , Automatic Quantitative and Qualitative Evaluation ,Online form to easily simulate realistic data using user-specified parameters .

Generating Data on the VLBI Imaging Website .

, Selecting/Uploading an Image . ,
, total flux density ( 2.5 ) ,
Rotation ( 180 ) .
Use SgrA* Model .
Spin : 0 % .
Inclination : 89 degrees .
Selecting Target Location and Field of View :
The requested domain can be searched through Wikipedia . 
Lets try :

Field of view center : 
Right = 17:45:40:401
Declination = 17:45:40:401
Field of view size : 
Right = 0.00016
Declination = 0.00016
Selecting Telescopes :
Add the telescope locations and intrinsic parameters that you would like to use to simulate data
Initilization: Select a pre-loaded telescope Name: Unique name for each telescope station (up to 12 characters)East Longitude/Latitude: East longitude and latitude of the array center. For locations less than 180 degrees west of Greenwich a minus sign should precede the longitude entry. X/Y/Z Position: Absolute X, Y, Z coordinates of each station (in meters) relative to the center of the Earth ,Lower/Upper Elevation: Lower and upper elevation limits of the of the antenna in degrees ,SEFD: System equivalent flux density of the antenna Diameter: Antenna diameter in meters .
Step 4: Specify Date and Time Data is Collected :
Specify the time of when you would like measurments to be taken, and the time interval between measurements. Start Time: Specify the time of your first observation in Universal Time (UT). The required format is “YYYY:ddd:hh:mm:ss” where YYYY is the year, ddd is the day number (e.g., December 31 is day 365); hh is the UT hour, mm is the UT minute, and ss is the UT second. Scan Duration: The length of a continuous scan in seconds Interval Length: The time in seconds between successive scans Number of Samples: The number of successive scans of this type .
Data Collection Settings :
Specify the center frequency and width of the observing channel in MHz.Center Frequency (MHz): 227297
Bandwidth (MHz): 4096 
Specify your integration time in seconds (sometimes referred to as “dump time” or “record length”). This is not the total duration of your observation, but rather the sampling and recording interval of the data. Integration Time (seconds): 60 .
What Kinds of Noise Can We Add?
Simulate Without Atmospheric Phase Errors .

And now we generally generate our data and downloaded .
What does the downloaded zip file provide ?
Original Images in FITS and PNG = ArryInfo
Plots to help you understand the data = Data
Data in a number of formats = Plots
Information to Reproduce Data = Sgraimage.fits
What are these data formats ? :
The primary data format that we have chosen to use is OIFITS. OIFITS is a standard for exchanging data for Optical (Visible/IR) Interferometry, and is based on the FITS Standard. Since mm/sub-mm VLBI shares a lot of similarities to optical interferometry, this format is better suited for mm/sub-mm measurements than UVFITS.
Table of files format Here .
Now you can try to generate photo from your data . just change the PATH of your data and image in source example.py in same folder .

Taj Alagawani 2019 - 2020 
