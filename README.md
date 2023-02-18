# CNN
MNIST images recognition with CNN

## CNN layers:

| ======================================= | ================ | ================ |
|-----------------------------------------|------------------|------------------|
| Layer (type:depth-idx)                  | Output Shape     | Param #          |
| ======================================= | ================ | ================ |
| ├─Sequential: 1-1                       | [-1, 32, 12, 12] | --               |
| └─Conv2d: 2-1                           | [-1, 32, 26, 26] | 832              |
| └─ReLU: 2-2                             | [-1, 32, 26, 26] | --               |
| └─Conv2d: 2-3                           | [-1, 64, 26, 26] | 18496            |
| └─ReLU: 2-4                             | [-1, 64, 26, 26] | --               |
| └─MaxPool2d: 2-5                        | [-1, 64, 13, 13] | --               |
| └─Conv2d: 2-6                           | [-1, 96, 13, 13] | 55392            |
| └─ReLU: 2-7                             | [-1, 96, 13, 13] | --               |
| └─Conv2d: 2-8                           | [-1, 64, 13, 13] | 55360            |
| └─ReLU: 2-9                             | [-1, 64, 13, 13] | --               |
| └─Conv2d: 2-10                          | [-1, 32, 13, 13] | 18464            |
| └─ReLU: 2-11                            | [-1, 32, 13, 13] | --               |
| └─Conv2d: 2-12                          | [-1, 32, 13, 13] | 9248             |
| └─ReLU: 2-13                            | [-1, 32, 13, 13] | --               |
| └─MaxPool2d: 2-14                       | [-1, 32, 12, 12] | --               |
| ├─Sequential: 1-2                       | [-1, 10]         | --               |
| └─Dropout: 2-15                         | [-1, 4608]       | --               |
| └─Linear: 2-16                          | [-1, 2048]       | 9439232          |
| └─ReLU: 2-17                            | [-1, 2048]       | --               |
| └─Dropout: 2-18                         | [-1, 2048]       | --               |
| └─Linear: 2-19                          | [-1, 1024]       | 2098176          |
| └─ReLU: 2-20                            | [-1, 1024]       | --               |
| └─Linear: 2-21                          | [-1, 10]         | 10250            |
| ======================================= | ================ | ================ |
| Total params: 11,705,450                                                      |
| Trainable params: 11,705,450            |                  |                  |
| Non-trainable params: 0                 |                  |                  |
| Total mult-adds (M): 59.61              |                  |                  |
| ======================================= | ================ | ================ |


## Steps
1. CrossEntropy Loss Criterion
2. Adam Optimizer with learning rate = 0.001
3. Training the model: 10 epochs with loss value 8.9e-08 at the last epoch
4. Evaluating results on **validation** set: **accuracy of 99%**
5. Evaluating results on **testing** set: **accuracy of 99%**
6. Saving the model for future transfer learning
