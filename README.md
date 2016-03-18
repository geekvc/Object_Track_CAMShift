
# ObjectTracker - CAMshift

##### Track multiple (10s - 100s) of objects in a video or a camera stream and define areas where entry of an object is to be monitored.
#

##### THIS USES THE LESS ACCURATE CAMshift ALGORITHM, COMPARE WITH ObjectTracker_Haar_Classifier FOR EXPLANATIONS
#
This enables the tracking of a mouse in an open field situation. The steps as also explained 
 [ here on the CV2 site:](http://www.swarthmore.edu/NatSci/mzucker1/opencv-2.4.10-docs/doc/tutorials/imgproc/histograms/back_projection/back_projection.html "CV2")




**Once initially (see A.):**
1. Take ROI Image 1
2. Calculate HS histogram for ROI

**For each other image (see B.):**

1. Get histogram for each pixel image n
2. Reference magnitude in Histogram 1
3. Replace pixel with magnitude to from Backprojected Histogram (see C.)

![OBJECTTRACKER_allobjects](http://i.imgur.com/pTNkVfi.jpg)


Then the Meanshift part of the algorithm will try to find the area with the highest density in pixels in the Backprojected Histogram, which, as these pixels indicate a match between Image1 and Image2, should be the most likely new position of our image.

![OBJECTTRACKER_allobjects](http://i.imgur.com/ESgW9zs.jpg)


If you run this file, for some example movie you will then end up with this rather shaky tracking (for explanations of the track and improvements, go look at file ObjectTrack_Haar_classifier)


![Link here](http://i.imgur.com/F3T5GKu.gif)




## What it does:
Creates data output in the form of images and also saves the raw data in .txt files.

Below is an example of the output of two tracked objects. The upper left image shows the speed of the objects, blue like colors depict
a slow speed, brighter colors a faster speed. At the top right the track of two objects (yellow and blue) is shown and three 
target areas that have been defined.

The bottom panel shows the times the different objects (yellow and blue) were inside target area 2.



*Output Example of all objects*
![OBJECTTRACKER_allobjects](http://i.imgur.com/Odb3XIc.png)



The next graphic shows the track, speed and position in the form of a heatmap of object 1.
The bottom panels show the distance object 1 covered during the tracking and the speed while tracked.

*Output Example of the details of the track object 1*
![OBJECTTRACKER_allobjects2](http://i.imgur.com/NgPeQgm.png)




##### Instructions are shown in the actual movie file or stream before it starts playing (eg see below).
![OBJECTTRACKER_allobjects2](http://i.imgur.com/eBl9VPK.png)





### To run you need python 2.7 and the following packages:

- cv2
- matplotlib
- pyplot
- numpy
- Tkinter

Download all files (click Download ZIP on the right), unzip and copy them into a folder YourFolder then you can run
the wrapper file do_track.py from the windows command prompt
```
c:YourFolder python do_track.py
```

I will work on some more fixes and then also generate a standalone executable file that does not need python.

emails to:
- <fuschro@gmail.com>