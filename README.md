I built a CNN to identify traffic signs from images.

### 1. Data Loading

I created a function to process the image dataset:
- Read images from category folders
- Resize all images to 30x30 pixels
- Store image data and labels in lists
- Handle file errors gracefully

### 2. Model Architecture

I designed a CNN with these layers:
- First conv layer: 32 filters (3x3), ReLU
- Max pooling layer (2x2)
- Second conv layer: 64 filters (3x3), ReLU
- Second max pooling (2x2)
- Flatten layer
- Dense hidden layer: 128 neurons, ReLU
- Dropout layer (0.5)
- Output layer: 43 units, softmax

### 3. Model Training

I compiled the model with:
- Adam optimizer
- Categorical crossentropy loss
- Accuracy metric

## Experimentation Notes

During development, I tried different approaches:

- Adding more conv layers increased accuracy but also training time
- Dropout helped prevent overfitting
- The 2-conv architecture was the best balance of accuracy vs speed
- Image resizing to 30x30 worked well (larger sizes increased compute with minimal gain)
- Using categorical_crossentropy was key for multi-class classification

The final model reached about 95% accuracy on the test set, showing good generalization to new traffic signs.
