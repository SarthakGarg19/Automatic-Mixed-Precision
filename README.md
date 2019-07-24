# Automatic-Mixed-Precision-
NVIDIA's Automatic Mixed Precision(AMP) is applied on a language model used for trigger word detection. Main aim is to find out if AMP helps the model to converge faster.

Training Dataset can be downloaded from https://drive.google.com/file/d/1---Wz0YoQ0xH6B4TP0IsUQnxRTVC9v5V/view?usp=drivesdk
XY_Train.zip can be downloaded from the link. You need to unzip this foldeer and put it inside the folder "Automatic-Mixed-Precision-"

Observations:-

1a. Trial 1 - Without AMP, loss = 1.2722, time = 86.03s (Batch Size = 64, Epochs=10, 5 layer model from scratch)

1b. Trial 1 - With AMP, loss = 0.6885, time = 100.596 (Batch Size = 64, Epochs=10, 5 layer model from scratch)

2a. Trial 2 - Without AMP, loss = 1.225, time = 127.96s (Batch Size = 32, Epochs=10, 5 layer model from scratch)

2b. Trial 2 - With AMP, loss = 0.6788, time = 150.20s (Batch Size = 32, Epochs=10, 5 layer model from scratch)

3a. Trial 3 - Without AMP, loss = 0.2695, time = 96.67s (Batch Size = 64, Epochs=10, Using PreTrained model)

3b. Trial 3 - With AMP, loss = 0.2833, time = 99.3s (Batch Size = 64, Epochs=10, Using PreTrained model)

4a. Trial 4 - Without AMP, loss = 0.180, time =90.58s (Batch Size = 64, Epochs=10, Both PreTrained model and 5 layer model)

4b. Trial 4 - With AMP, loss = 0.280 , time = 103.46s (Batch Size = 64, Epochs=10, Both PreTrained model and 5 layer model)
