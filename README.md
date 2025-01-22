TIMEMAP:

1) Research: I watched a lot of videos on youtube and read about vision transofrmers first since i had just completed a task prior to it,but soon i found out that the dataset would be too small to perform image classification using image transformers. Then I started learning about CNN's and settled on making a custom CNN to perform image classification.

2) Execution:

I started with a simple CNN model that had just one convolutional layer and one dense layer.
As I progressed, I expanded the architecture by adding more convolutional layers with increasing filters (32, 64, and 128) to capture more complex patterns from the images.
After each convolutional layer, I added batch normalization to stabilize and speed up the training process.
I also added MaxPooling layers after each convolutional block to reduce the spatial dimensions of the data while retaining important features.
Dense Layers and Dropout.

I introduced additional fully connected dense layers (e.g., with 256 and 512 units) after flattening the convolutional layers, using ReLU activation.
To combat overfitting, I added dropout layers, using a dropout rate of 0.5 to randomly drop connections during training and improve generalization.
Regularization:

I added L2 regularization to the dense layers to penalize large weights and help the model generalize better.
I experimented with different regularization strengths, adjusting it from 0.01 to 0.001.
Optimizer Customization:

I modified the Adam optimizer by setting a custom learning rate (e.g., 0.0001) to better control the learning speed and improve convergence.

Model Compilation:

I kept using sparse_categorical_crossentropy for multi-class classification and accuracy as the evaluation metric.
Pre-trained Model Integration:

I experimented with various image augmentation techniques to generate more training data, given the relatively small size of my dataset.
I used Augmentor to apply rotations, flips, zooming, and random distortions.
Later in the process, I applied more extreme augmentation techniques, such as blurring and random erasing, to improve the model’s robustness to variations in the input data.

Training and Validation Setup:

I tried different train-validation splits before finally settling on an 80/20 split.
I also generated additional data through augmentation to reduce overfitting and improve my model’s overall performance.


3)Conclusion:


I created a model that is very close to mobilenet and beats resnet 50 in its accuracy.
