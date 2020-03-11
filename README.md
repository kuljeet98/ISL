# ISL
In OpenPose_video(1).ipynb file the Openpose Library is used to convert the videos and to detect the hands and to convert the background color to black. 
The logic used to iterate over the files in the specific folder is :

for video in os.listdir('/content/'): #content is the location where the videos are available.
  if video.endswith(".mp4"):  #checking the format of the type and specifically choosing video files
    !cd openpose && ./build/examples/openpose/openpose.bin --video /content/$video --write_json /output/ --display 0 --write_video output/$video --disable_blending  --hand
 
 And the command used to copy the files to the drive is:
 
 import shutil
srdir = '/content/openpose/output/'
for videos in os.listdir(srdir):
  if videos.endswith(".mp4"):
    shutil.copy(srdir+videos,'/content/drive/My Drive/PROJECT_DATA/OpenPose/tuesday')

#Renaming.ipynb
This file is to rename the different pattern named videos to same pattern named videos. Firstly, some of the videos names were like Monday001.mp4 and rest were like MONDAY1.mp4. Now I have renamed all those videos into the same named videos like Monday_1.mp4 And the counter keeps on incrementing for every video.
