# Video-Survelliance-System
We prepared a project which aims at ACTION RECOGNITION(mainly Sports Classes). We trained a VGG-16 Neural Network along with LSTM with UCF-101 Dataset having 101 classes. Initially, Dense Optical Flow was applied on the Dataset Videos and then respective MAGNITUDE and ANGLES were fed to the VGG-LSTM Network. After which the predictions of Networks processing angle and magnitudes are fused to get a single output.

Data extraction.ipynb focus on considering the videos and extracting features between every two consecutive frames and converting them into corresponding magnitide and angle matrices.
The matrices were then stored in a list and stored in separate csv files for Magnitude and Angle Matrices. 
The matrices where then interpolated to reduce the size from (240,320) to (224,224) and then to (224,224,3) by duplicating the channels.
These were then fed To the CNN-LSTM Network, Two networks were trained each for the slope and magnitude matrices.
The outputs of the two networks were then fused to get a final output.
An IOT System was also integrated with it to update the user with emails or SMS if some anomaly activity is detected.
