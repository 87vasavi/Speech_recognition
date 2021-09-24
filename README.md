## Problem Statement :
Count number of speakers and speaker's gender from recorded audio .mp3/.wav files

### Approach :
- To compare audios we need some features of the audio that are to be extracted and store in some numpy array format. 
- Here I took mfcc, chroma, mel, tonnetz features avg value of an audio file and stored them in result array. 
- I used RAVDESS dataset and I gave the equal number of male and female voice dataset set to train and acheived an accuracy of 99%.
- Used Multi layer perceptron Classifier(MLPClassifier) to train and test the model.
#### Improvements in Approach:
- Dataset to be choosen from librosa predefined dataset which contain different voices in an audio file.
- we need to split the audio file when the speaker is changed and we can use the above model we created to detect the gender.
- for Speaker change detection we can use 1class SVM model.
- The speaker can speak more than once so, Speaker Diarization should be done.
- for every new speaker we increment the count and store the gender of the speakers in a dictionary.
