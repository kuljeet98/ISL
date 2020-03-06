#### indian Sign Language detection using openpose
```
clone the github repository for installing the openpose 
git_repo_url = 'https://github.com/CMU-Perceptual-Computing-Lab/openpose.git
```
f is the list which denotes the videoname i.e monday001.mp4
subprocess usage:
```
! rm *.mp4
'''video path from drive to /content'''
for i in range(0,len(f)):
  subprocess.call(["ffmpeg","-i",sourcedir+f[i], f[i]])
'''openpose convertion'''
for i in f:  
  !cd openpose && ./build/examples/openpose/openpose.bin --video ../$i --write_json ./output/ --display 0 --write_video ../$i --disable_blending  --hand
  ```
