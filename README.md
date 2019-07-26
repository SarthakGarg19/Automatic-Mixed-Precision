# Automatic-Mixed-Precision-
NVIDIA's Automatic Mixed Precision(AMP) is applied on a model used for trigger word detection using convolution layer and GRU. Main aim is to find out if AMP helps the model to converge faster.

Download the train data from https://drive.google.com/file/d/1---Wz0YoQ0xH6B4TP0IsUQnxRTVC9v5V/view?usp=drivesdk if you want to follow along the notebook.

Extract XY_train folder to the root of the project directory.


In the files written as "AMP ASR Trial x" we are enabling Automatic Mixed Precision and in the files written as "ASR Trian x" we are not using Automatic Mixed Precision.
For eg. Code is same for "ASR Trial 2" and "AMP ASR Trial 2", except "AMP ASR Trial 2" has an added line of code where Automatic Mixed Precision is being enabled.

Observations:-

1. AMP ASR Trial 1, A 5 layer language model is built from scratch and for training we are using Automatic Mixed Precision Technique with the following hyperparameters "Batch Size = 64, Epochs = 10" Results are as follows "loss = 0.6885, time = 100.596"

2. ASR Trial 1, A 5 layer language model is built from scratch and for training with the following hyperparameters "Batch Size = 64, Epochs = 10" Results are as follows "loss = 1.2722, time = 86.03s"

3. AMP ASR Trial 2, A 5 layer language model is built from scratch and for training we are using Automatic Mixed Precision Technique with the following hyperparameters "Batch Size = 32, Epochs=10" Results are as follows  "loss = 0.6788, time = 150.20s"

4. ASR Trial 2, A 5 layer language model is built from scratch and for training with the following hyperparameters "Batch Size = 32, Epochs=10" Results are as follows "loss = 1.225, time = 127.96s"

5. AMP ASR Trial 3, A pretrained model is loaded and compiled and is trained with  XY_train with using Automatic Mixed Precision Technique with the following hyperparameters "Batch Size = 64, Epochs=10" Results are as follows  "loss = 0.2833, time = 99.3s"

6. ASR Trial 3, A pretrained model is loaded and compiled and is trained with XY_train with the following hyperparameters "Batch Size = 64, Epochs=10" Results are as follows "loss = 0.2695, time = 96.67s"
