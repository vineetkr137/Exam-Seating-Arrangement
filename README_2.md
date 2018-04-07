## INSTALLATION OF YOLO USING POINTGREY/FLYCAPTURE CAMERA ON INTEL PROCESSOR

## TOOLS AND REQUIREMENTS:
opencv 3.3.0
Flycapture sdk 2.11.3.*


## INSTALLATION STEPS:
### 1.  Clone from github repository
       $  git clone -b vineet_devlop https://github.com/DreamVu/MVP_Software.git 

### 2.  Get into directory.
       $  cd Flycapture_intel/

### 3.  Run make file command.
       $  make
### 4. Download yolo.weights from google drive. 
     wget https://drive.google.com/open?id=173rsGNOFoPuTjajTTRushMGvL9cQldo-

### 5. Download calibration file 
    wget https://drive.google.com/open?id=1K9yy0Mc94X_NqdIG_GTmQskLFcXmWM71

### 6.  Create  a bash file in the directory ‘yolo.sh’.
Copy into bash file
        	 
               #!/bin/bash
               
               start=`./darknet detect cfg/yolo.cfg yolo.weights`
               
               echo $start

### 7.   Make  shell script executable.
   $ chmod u+x yolo.sh

### 8.   Make a shell script on Desktop to direct run yolo from desktop
 Copy into new bash file on Desktop.
              
              #!/bin/bash
              
        	start= $( cd  /path/to/executable/bash/script/   ; sh yolo.sh )
     	
              echo $start  
### 9.   Make  shell script executable on Desktop.
     $ chmod u+x yolo.sh

### 10.   Change preference of executable script to ‘ask everytime’.

### 11.  To run yolo double click on desktop executable and than ‘Run in Terminal’.
