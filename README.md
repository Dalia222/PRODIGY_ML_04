# PRODIGY_ML_04 - GestureCraft: Building a Robust Hand Gesture Recognition Model for Enhanced Human-Computer Interaction and Gesture-Based Control Systems

## Data Analysis
```python
Shape of the first image: (50, 50)
Class index of the first image: 0
```
## Shuffle & Plot Data
![Plotting shuffled data](https://i.postimg.cc/PrhFcr3j/Shuffled-data-plotting.png)

## Normalization
```python
Shape of the data: (20000, 50, 50)
```
## Building The model
```python
Epoch 1/7
438/438 [==============================] - 142s 324ms/step - loss: 0.0024 - accuracy: 0.9992 - val_loss: 3.0895e-04 - val_accuracy: 1.0000
Epoch 2/7
438/438 [==============================] - 125s 285ms/step - loss: 0.0037 - accuracy: 0.9989 - val_loss: 2.4960e-04 - val_accuracy: 1.0000
Epoch 3/7
438/438 [==============================] - 132s 302ms/step - loss: 1.4798e-05 - accuracy: 1.0000 - val_loss: 5.5529e-05 - val_accuracy: 1.0000
Epoch 4/7
438/438 [==============================] - 125s 285ms/step - loss: 0.0015 - accuracy: 0.9994 - val_loss: 2.0319e-04 - val_accuracy: 1.0000
Epoch 5/7
438/438 [==============================] - 129s 296ms/step - loss: 1.6047e-04 - accuracy: 1.0000 - val_loss: 2.6884e-04 - val_accuracy: 0.9997
Epoch 6/7
438/438 [==============================] - 137s 313ms/step - loss: 4.9368e-04 - accuracy: 0.9999 - val_loss: 8.5435e-05 - val_accuracy: 1.0000
Epoch 7/7
438/438 [==============================] - 125s 285ms/step - loss: 3.5496e-04 - accuracy: 0.9999 - val_loss: 0.0021 - val_accuracy: 0.9993
```
## Training History Plot
![Training History plot](https://i.postimg.cc/fWYrB0vC/Training-histoey-plot.png)

## Model Summary
```python
Model: "sequential"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d (Conv2D)             (None, 48, 48, 32)        320       
                                                                 
 activation (Activation)     (None, 48, 48, 32)        0         
                                                                 
 conv2d_1 (Conv2D)           (None, 46, 46, 32)        9248      
                                                                 
 activation_1 (Activation)   (None, 46, 46, 32)        0         
                                                                 
 max_pooling2d (MaxPooling2  (None, 23, 23, 32)        0         
 D)                                                              
                                                                 
 dropout (Dropout)           (None, 23, 23, 32)        0         
                                                                 
 conv2d_2 (Conv2D)           (None, 21, 21, 64)        18496     
                                                                 
 activation_2 (Activation)   (None, 21, 21, 64)        0         
                                                                 
 max_pooling2d_1 (MaxPoolin  (None, 10, 10, 64)        0         
 g2D)                                                            
                                                                 
 dropout_1 (Dropout)         (None, 10, 10, 64)        0         
                                                                 
 flatten (Flatten)           (None, 6400)              0         
                                                                 
 dense (Dense)               (None, 256)               1638656   
                                                                 
 dense_1 (Dense)             (None, 10)                2570      
                                                                 
=================================================================
Total params: 1669290 (6.37 MB)
Trainable params: 1669290 (6.37 MB)
Non-trainable params: 0 (0.00 Byte)
_________________________________________________________________
```
## Confusion Matrix
![Confusion Matrix](https://i.postimg.cc/3NjfRPwV/Confusion-matrix.png)

## Unique Class Labelling
![Class Unique Labelling](https://i.postimg.cc/ZnzDJTJ6/Class-labelling.png)
