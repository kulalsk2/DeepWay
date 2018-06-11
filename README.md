# DeepWay
This project is an aid to the blind. Till date there has been no technological advancement in the way the blind navigate. So I have used deep learning particularly convolutional neural networks so that they can navigate through the streets. 
# My Approach 
## Collecting Training Data
My project is an implementation of CNN's, and we all know that they require a large amount of training data. So the first obstruction in my way was a correclty labeled dataset of images. So I went around my college and recorded a lot of videos(of all types of roads and also offroads).Then I wrote a basic python script to collect save images from the video(I saved 1 image out of every 5, because the consecutive frame are almost identical). I collected almost 10000 such images almost 3300 for each class(i.e. left right and center). 
<br>Left image:</br>
![274](https://user-images.githubusercontent.com/24778913/41227028-10cf6888-6d91-11e8-805a-bef4814ed1c1.jpg)
<br>Right Image:</br>
![11](https://user-images.githubusercontent.com/24778913/41227057-2e4b95bc-6d91-11e8-83ff-4744bcf49382.jpg)
<br>Center Image:</br>
![146](https://user-images.githubusercontent.com/24778913/41227081-42005b88-6d91-11e8-8de5-6ee415d8f617.jpg)




## Training the Model
I made a collection of CNN architectures and trained the model. Then I evaluated the performance of all the models and chose the one with the best accuracy. I got a training accuracy of about 97%
The architecture of the best model was:


##
   ![screenshot 247](https://user-images.githubusercontent.com/24778913/41226545-6982ca30-6d8f-11e8-88d2-b771b3647e54.png)
   ##
   
## Interfacing with the Arduino
The next problem was how can I tell the blind people in which direction to move .
So I connected my python program to an Arduino. I connected the servo motors to arduino and fixed the servo motors to the sides of an spectacle.  Using Serial communication I can tell the arduino which servo motor to move which would then press to one side of the blind person's head and would indicate him in which direction to move.<br> This is how the modified spectacles looked like</br>
![imag0397](https://user-images.githubusercontent.com/24778913/41227853-ec3f52fa-6d93-11e8-9760-6dcbd931fd4f.jpg)

## Other Features
#
<br>Detection of stop signs.</br> This is done using opencv. I load in a pretrained stop sign haar cascade and then identify the location of the stop sign so that the device can steer the blind person.
#
<br>Person and Vehicle Detection</br>
This is achieved by using the yolo algorithm.I did not implement this, I am just using the object detected by yolo to make the person aware of his surrounding.

## Requirements
0. Python 3.x
1. <a href="https://tensorflow.org">Tensorflow 1.5</a>
2. <a href="https://keras.io">Keras</a>
3. OpenCV 3.4
4. h5py
5. pyttsx3
6. A good grasp over convolutional neural networks. For online resources refer to standford cs231n, deeplearning.ai on coursera
7. A good CPU (preferably with a GPU).
8. Time
9. datetime
10. Patience.... A lot of it.

## Installing the requirements
1. Start your terminal of cmd depending on your os.
  2. If you have a NVidia GPU then make sure you have the prerequisites for Tensorflow GPU installation (Refer to official site). Then use this commmand

    pip install -r requirements_gpu.txt

  3. In case you do not have a GPU then use this command

    pip install -r requirements_cpu.txt



