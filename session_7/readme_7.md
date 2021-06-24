**Assignment**:

Submit the Assignment 5 as Assignment 
1. To be clear,ONLY use datasetSentences.txt. (no augmentation required)
2. Your dataset must have around 12k examples.
3. Split Dataset into 70/30 Train and Test (no validation)
4. Convert floating-point labels into 5 classes (0-0.2, 0.2-0.4, 0.4-0.6, 0.6-0.8, 0.8-1.0) 
5. Upload to github and proceed to answer these questions asked in the S7 - Assignment Solutions, where these questions are asked:
6. Share the link to your github repo (100 pts for code quality/file structure/model accuracy)
7. Share the link to your readme file (200 points for proper readme file)
8. Copy-paste the code related to your dataset preparation (100 pts)
9. Share your training log text (you MUST have been testing for test accuracy after every epoch) (200 pts)
10. Share the prediction on 10 samples picked from the test dataset. (100 pts)

**Approach:**

Dataset Vocabulary
![Dataset Vocabulary](https://github.com/JahnaviRamagiri/END2.0/blob/main/Session-5%20Sentiment%20Analysis%20using%20LSTM%20RNN/images/vocabulary.png)

total samples : 11.2k
split into training and validation 70:30 - 7900, 3386 samples respectively

converted floating values to 5 calsses using mapping function 
def mapping_output(x):
  if 0<x<0.2:
    return 0
  elif 0.2<x<0.4:
    return 1
  elif 0.4<x<0.6:
    return 2
  elif 0.6<x<0.8:
    return 3
  else:
    return 4

**Model** 

Model Parameters
![Model Parameters](https://github.com/JahnaviRamagiri/END2.0/blob/main/Session-5%20Sentiment%20Analysis%20using%20LSTM%20RNN/images/model_param.png)

**Results and Accuracy**:



Accuracy Curve Without Augmentation
![accuracy curve without augmentation](https://github.com/JahnaviRamagiri/END2.0/blob/main/Session-5%20Sentiment%20Analysis%20using%20LSTM%20RNN/images/without_augmentation.png)



Test Results:
![image](https://github.com/JahnaviRamagiri/END2.0/blob/main/Session-5%20Sentiment%20Analysis%20using%20LSTM%20RNN/images/test_results.PNG)


**Code ref link**:

https://github.com/kotalaraghava/END-2.0---school-of-ai/blob/master/session_5/Sentiment_Analysis_using_LSTM_RNN.ipynb
