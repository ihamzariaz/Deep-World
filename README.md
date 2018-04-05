# Deep-World
# First project in Deep-World environment.
# 1) YOLO_2 DarkNet Implimentation on our own dataset on gpu.
Setp 1:
before this step you have to make sure that your system must have navidia gpu support and opencv running in it for better results.
Install darket in your ubuntu machine server with modification in makefile such as
GPU=1;
OpenCv=1;
Step 2:
Collect the data on which we want to train over network and images size is not an issue according to our experiences because we trained yolo_2 on 720*1280 resolution.
Step 3:
Finding the labeling tool to label our dataset and after doing hard search we find and labeling tool. This labeling tool can label the multi classes and it is so much user friendly. The following link will expalain how to use it.
Step 4:
After labeling, we have to make changes the cfg file in the cfg directory in darknet and we will create data file and place it the data directory. The obj.data file look like this:   
classes= 2
train  = data/train.txt
valid  = data/test.txt
names = data/obj.names
backup = backup
results= results
Now, create obj.names file in data directory which have the name of classes according to labeling sequence.
car
back_side
Step 5:
Path generation code for test and train datasets.

You need to run this code in the same directory which contains your dataset.

