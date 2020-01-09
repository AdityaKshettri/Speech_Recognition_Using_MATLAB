# Speech_Recognition_Using_MATLAB
Implementation of Speech Recognition System in MATLAB Environment using Correlation as well as using MFCC and DTW Algorithms.

# Abstract :

In this project, Speech recognition system in MATLAB environment is explained. Mel-Frequency Cepstral Coefficients (MFCC) and Dynamic Time Wrapping (DTW) are two algorithms adapted for feature extraction and pattern matching respectively. When the user utters something, it is sent to the speech engine to be processed then converted into digital domain. The digitalized speech samples are processed to extract features using MFCC algorithm. Once the desired number of features is obtained, they can be sent through feature matching stage where DTW is used for comparison between saved templates and recorded speech. Results are obtained by one time training and continuous testing phases.

# Speech Recognition :

Speech recognition algorithms can be broadly divided into speaker dependent and speaker independent. Speaker dependent system focuses on developing a system to recognize unique voiceprint of individuals. Speaker independent system involves identifying the word uttered by the speaker. It can be further classified into isolated word detection and continuous speech recognition. Input for isolated word detection is single words separated by pauses. This is relatively simpler compared to continuous speech recognition as the system doesn’t need to learn fluidic sequence of dictionary words. Continuous speech recognition can be used in security systems for verifying password uttered by the user. Speech recognition system processes the word uttered by the user and generates its features. This entire system is implemented in MATLAB environment where the speech samples input are recorded through windows sound card.

A- Recognition Module

Isolated word detection involves two digital signal processes which are Feature Extraction and Feature Matching.
Feature extraction involves calculation of MFCCs for each frame. MFCCs are the coefficients that collectively represent the short-term power spectrum of a sound, based on a linear cosine transform of a log power spectrum on a nonlinear MEL scale of frequency. 
For feature matching DTW method is used.

B. Feature Extraction (MFCC)

MFCC is based on human hearing perceptions which cannot perceive frequencies over 1KHz. Features obtained by MFCC algorithm are similar to known variation of the human cochlea’s critical bandwidth with frequency. The process extracting MFCCs for a given voice sample is shown in Figure.

C. Feature Matching (DTW)

In this stage, the features of word calculated in previous step are compared with reference templates. DTW algorithm is implemented to calculate least distance between features of word uttered and reference templates. Corresponding to least value among calculated scores with each template, the word is detected. DTW finds the optimal alignment between two times series if one time series may be “warped” non-linearly by stretching or shrinking it along its time axis. The extent of matching between two time series is measured in terms of distance factor.
