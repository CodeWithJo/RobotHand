# RobotHand
AUDIO DATA COLLECTION
  Find a way to collect audio data from different people for a more robust model. I am woking with about 70 audio .wav files per word
  If they can give you the audio data in .wav , convert it from mp3 mp4 ogg etc to .wav
  I use Audacity for the data clean up and an online coverter for the data conversion.
  Make sure the are 16000hz and 1 second long else ajust the python curation script to suit your range.

AUDIO DATA CURATION
  The Python script found at 
  https://github.com/ShawnHymel/ei-keyword-spotting.git
  this help add some low level backgroud noice to the data and generated a larger number of test samples from the data you have , 
  I generated 1500 .wav file form every phrase
  
AUDIO DATA UPLOAD ,FEATURE EXTRATION AND  MODEL TRAINING 
  Create a edge impulse developer account.
  https://edgeimpulse.com/
  Using Edge impulse
  Load the data and extra the features using MFCC
  Train a neural network to perform basic keyword spotting, 
    -I used the  Clasification with Karas
    -100 training cycles 
    -0.005 for the learning rate
    -And used 20 percent of the total data as validation/test set 
   
  Additional parameters
     -Input layer has 650 features
     -One Dimension  convolution / pool layer (8 neurons, 3 kernel size, 1 layer)
     -Dropout rate 0.25
     -Output layer has 10 classes
       
MODEL TESTING 
The 20% data that was not used for training i used it for testing the model
you can change the confidence level, i left it at the default 0.6


ROBOT HAND DESIGN
I have used the iMoov robot hanf and forarm 3D designs 
http://inmoov.fr/hand-and-forarm/

RESULTS 
to access the online classifier go to https://smartphone.edgeimpulse.com/classifier.html
to access the full project report , videos and analysis go to https://moose-magenta-dtng.squarespace.com/
to access the robot hand code go to https://github.com/CodeWithJo/RobotHand.git
