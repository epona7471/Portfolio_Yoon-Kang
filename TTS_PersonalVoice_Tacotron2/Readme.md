End-to-End TTS personal voice generator using Nvidia Tacotron2
=============

This Model follows the tutorial of 'Voice Deepfake with Tacotron 2 for beginners tutorial'([Link](https://www.youtube.com/watch?v=gVqSEIr2PD4)). This project comes with extra personal-voice recording part. For more details at 'Your_Voice_recorder.ipynb'

## 1. Dataset

- How to record your personal speech data
   1. Open 'Your_Voice_recorder.ipynb' on Google Colab 
   2. Set the value of variable 'count' which sets the size of the speech dataset
   3. Before recording every sentence, there is 3 second stanby time. While then, please check the following script and prepare for recording.   
   4. After 3 sec, you can see the new message 'Starting recording for (6) seconds...', which mean recording has started.
   5. Read the popped sentence loudly and clearly. If recording time is too short, you can change the 'record_seconds' value longer.

## 2. Training & Synthesis 

1) Model training (Follow instructions at Tacotron2_Training.ipynb)  
 
   ![image](https://user-images.githubusercontent.com/13134929/134140263-33fd0890-d2e8-450e-8977-32a79c3c5fba.png)

2) Synthesis (Follow instructions at Tacotron2_Synthesis.ipynb)   

   ![image](https://user-images.githubusercontent.com/13134929/134140641-89b6aab9-803b-48a8-b487-5e020472e8eb.png)

## 3. Further study
  New recording methods are being considered to improve the quality of raw data. The result will be compared to voice cloning project.
