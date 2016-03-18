#ObjectTracker

#####Track multiple (10s - 100s) of objects in a video or a camera stream and define areas where entry of an object is to be monitored.

THIS USES THE LESS ACCURATE CAMshift ALGORITHM, COMPARE WITH ObjectTracker_Haar_Classifier FOR EXPLANATIONS

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




#####Instructions are shown in the actual movie file or stream before it starts playing (eg see below).
![OBJECTTRACKER_allobjects2](http://i.imgur.com/eBl9VPK.png)



Currently only color files are supported, it does not yet work with grayscale files.


###To run you need python2 and the following packages:
cv2
matplotlib
pyplot
numpy
Tkinter

Download all files (click Download ZIP on the right), unzip and copy them into a folder YourFolder then you can run
the wrapper file do_track.py from the windows command prompt
```
c:YourFolder python do_track.py
```

I will work on some more fixes and then also generate a standalone executable file that does not need python.

emails to:
- <fuschro@gmail.com>