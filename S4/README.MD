Assignment:
Refer to this code: COLABLINK (Links to an external site.)
WRITE IT AGAIN SUCH THAT IT ACHIEVES
1. 99.4% validation accuracy
2. Less than 20k Parameters
3. You can use anything from above you want. 
4. Less than 20 Epochs
5. No fully connected layer

To learn how to add different things we covered in this session, 
you can refer to this code: https://www.kaggle.com/enwei26/mnist-digits-pytorch-cnn-99 (Links to an external site.) 

1. My belief of more number of nodes in hidden layers make the model better was shattered. The way you design it 
   matters more in the performance of the model.
2. Used a 1*1 convolution in the end to get required number of channels.
3. Learning that we can go from 8 to 16 in a laye and reduce the 16 to 8 by using 1*1 convolution, which I felt will help model
   in a better learning.
4. Batch Normalization actually amazed me with performance improvement by the way it highlights the feature. I dont think this
   accuracy possible without it.
5. I used Dropout only to get the final edge accuracy of .4 or something.

----------------------------------------------------------------
        Layer (type)               Output Shape         Param
----------------------------------------------------------------
            Conv2d-1            [-1, 8, 26, 26]              72
           Dropout-2            [-1, 8, 26, 26]               0
       BatchNorm2d-3            [-1, 8, 26, 26]              16
            Conv2d-4            [-1, 8, 24, 24]             576
           Dropout-5            [-1, 8, 24, 24]               0
       BatchNorm2d-6            [-1, 8, 24, 24]              16
            Conv2d-7            [-1, 8, 22, 22]             576
           Dropout-8            [-1, 8, 22, 22]               0
       BatchNorm2d-9            [-1, 8, 22, 22]              16
           Conv2d-10            [-1, 8, 20, 20]             576
          Dropout-11            [-1, 8, 20, 20]               0
      BatchNorm2d-12            [-1, 8, 20, 20]              16
        MaxPool2d-13            [-1, 8, 10, 10]               0
           Conv2d-14             [-1, 16, 8, 8]           1,152
          Dropout-15             [-1, 16, 8, 8]               0
      BatchNorm2d-16             [-1, 16, 8, 8]              32
           Conv2d-17             [-1, 16, 6, 6]           2,304
          Dropout-18             [-1, 16, 6, 6]               0
      BatchNorm2d-19             [-1, 16, 6, 6]              32
           Conv2d-20             [-1, 16, 4, 4]           2,304
          Dropout-21             [-1, 16, 4, 4]               0
      BatchNorm2d-22             [-1, 16, 4, 4]              32
           Conv2d-23             [-1, 16, 2, 2]           2,304
          Dropout-24             [-1, 16, 2, 2]               0
      BatchNorm2d-25             [-1, 16, 2, 2]              32
           Conv2d-26             [-1, 10, 2, 2]             160
----------------------------------------------------------------
Total params: 10,216
Trainable params: 10,216
Non-trainable params: 0
-----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.44
Params size (MB): 0.04
Estimated Total Size (MB): 0.48
----------------------------------------------------------------

