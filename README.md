Image Processing and CNN Model

Image Filtering

Edge Detection using Sobel Operator

Edge detection is a technique used to identify the boundaries of objects in an image. The Sobel operator is a widely used method for detecting edges in a specific direction. Below are the Sobel kernels used for detecting vertical and horizontal edges:

Vertical Edge Detection Kernel:

Kx = [[-1, -2, -1],
      [ 0,  0,  0],
      [ 1,  2,  1]]

Horizontal Edge Detection Kernel:

Ky = [[-1,  0,  1],
      [-2,  0,  2],
      [-1,  0,  1]]

A script is provided that applies the Sobel operator to an input image and displays:

The original image

The Sobel X image (detects vertical edges)

The Sobel Y image (detects horizontal edges)

Corner Detection

Corner detection is used to identify points in an image where the intensity gradient has large variations in multiple directions. The script provided implements corner detection using predefined kernels discussed in the lecture slides.

Image Scaling

After blurring an image, different scaling techniques can be applied to reduce its resolution while maintaining its key features:

2x2 scaling

4x4 scaling

A script is available to test and visualize the effects of these scaling techniques on a sample image.

Build CNN Model for CIFAR-10 Classification

Model Definition

The CNN model implemented for CIFAR-10 classification consists of:

Three convolutional layers with ReLU activation and max pooling.

Fully connected layers for classification.

Dropout layers to prevent overfitting.

Training Process

The model is trained using CrossEntropyLoss and optimized using both Adam and SGD with momentum. The training loop includes:

Forward propagation

Loss computation

Backpropagation

Weight updates

Early stopping to prevent overfitting

Training Results

Epoch Count: 30 (with early stopping)

Training loss and validation loss monitored for overfitting

Best model saved after achieving lowest validation loss

Testing and Performance Evaluation

The trained model was evaluated on unseen test data, yielding:

Test Loss: 0.790509

Overall Test Accuracy: 73.08%

Class-wise Accuracy:

Airplane: 79.90%

Automobile: 91.10%

Bird: 63.90%

Cat: 49.30%

Deer: 73.40%

Dog: 69.10%

Frog: 79.90%

Horse: 69.40%

Ship: 82.70%

Truck: 72.10%
