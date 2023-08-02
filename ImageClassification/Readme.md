# Impressive Image Classification Model

## Overview

This project involves an image classification model that utilizes Convolutional Neural Networks (CNN), Data Augmentation, and Distributed Training strategies. The model achieves a **Test Accuracy of 63.52%**, which is impressive given the complexity of the image dataset.

!\[Model Overview](![image](https://github.com/Luke-J-Miller/Showcase/assets/111100132/7754d04f-4ac5-42a2-ba55-af69ac427c5f)
) (*The structure of the classification model.*)

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

Here's a glimpse of our model:

```python
model = build_model()  # function which returns the model defined above
```

## Compilation and Training

The model is compiled with the Adam optimizer, categorical cross-entropy loss, and accuracy metric.

```python
opt = optimizers.Adam(learning_rate=0.001)
model.compile(optimizer=opt, loss='categorical_crossentropy', metrics=['accuracy'])
```

We then train the model with distributed training strategy for 50 epochs and a batch size of 64, with early stopping monitoring the validation loss.

```python
with strategy.scope():
    history = model.fit(
        data_gen.flow(x_train, y_train, batch_size=batch_size),
        steps_per_epoch=len(x_train) / batch_size,
        epochs=epochs,
        validation_data=(x_test, y_test),
        callbacks=[early_stopping]
    )
```

## Results

Our model achieved a **Test Accuracy of 63.52%**. 

!\[Model Accuracy](![image](https://github.com/Luke-J-Miller/Showcase/assets/111100132/2e91b117-ceb8-4e14-bcd9-600682aa60b0)
) (*Model accuracy over epochs.*)

The model loss over epochs is shown below:

!\[Model Loss](![image](https://github.com/Luke-J-Miller/Showcase/assets/111100132/9503fc72-9390-4df0-9438-e9ce4535a876)
) (*Model loss over epochs.*)