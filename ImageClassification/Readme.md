# CIFAR-10 Image Classification Model

## Overview

This project involves an image classification model that utilizes Convolutional Neural Networks (CNN), Data Augmentation, and Distributed Training strategies. The model achieves a **Test Accuracy of 63.52%**, which is impressive given the complexity of the image dataset.


## Data Augmentation

To improve the performance of our model, we use data augmentation, a technique that expands our training dataset with variations of the original images. This is done using Keras's ImageDataGenerator, which performs random transformations on the images, such as rotation, shifts, and flips.

```python
data_gen = image.ImageDataGenerator(
    rotation_range=15,
    width_shift_range=0.1,
    height_shift_range=0.1,
    horizontal_flip=True,
)
data_gen.fit(x_train)
```

## Model Architecture

Our model architecture comprises several Convolutional layers, each followed by Batch Normalization and then a Max Pooling layer. The use of Dropout at several stages reduces the risk of overfitting. The final Dense layer employs a softmax activation function to provide the output classification.

![image](https://github.com/Luke-J-Miller/Showcase/assets/111100132/7754d04f-4ac5-42a2-ba55-af69ac427c5f)
 
## Compilation and Training

The model is compiled with the Adam optimizer, categorical cross-entropy loss, and accuracy metric. We then train the model with distributed training strategy for 50 epochs and a batch size of 64, with early stopping monitoring the validation loss.

```python
with strategy.scope():
    epochs = 50
    batch_size = 64
    early_stopping = callbacks.EarlyStopping(monitor='val_loss', patience=10)
    model = build_model()
    # Adjust optimizer for mixed precision training
    opt = optimizers.Adam(learning_rate=0.001)
    #opt = tf.keras.mixed_precision.LossScaleOptimizer(opt)
    
    model.compile(optimizer=opt,
                  loss='categorical_crossentropy',
                  metrics=['accuracy'])
```

## Results

Our model achieved a **Test Accuracy of 63.52%**. 

![image](https://github.com/Luke-J-Miller/Showcase/assets/111100132/2e91b117-ceb8-4e14-bcd9-600682aa60b0)
 

The model loss over epochs is shown below:

![image](https://github.com/Luke-J-Miller/Showcase/assets/111100132/9503fc72-9390-4df0-9438-e9ce4535a876)
 
