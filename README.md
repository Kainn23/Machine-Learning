1. Research Phase
Initially, I explored Vision Transformers by watching several tutorials on YouTube and reading relevant articles, as I had recently completed a related task. However, I soon realized that the dataset I was working with was too small to effectively train an image classification model using transformer-based architectures. As a result, I shifted my focus to Convolutional Neural Networks (CNNs) and decided to design a custom CNN model tailored for image classification tasks.

2. Execution Phase
Initial Model Development:

I began with a basic CNN architecture consisting of a single convolutional layer followed by a dense layer.

Gradually, I expanded the model by adding multiple convolutional layers with increasing filter sizes (32, 64, and 128) to capture more complex and hierarchical features from the input images.

Batch Normalization was incorporated after each convolutional layer to enhance training stability and accelerate convergence.

MaxPooling layers were added after each convolutional block to reduce spatial dimensions while preserving significant features.

Fully Connected Layers and Dropout:

After flattening the output from the convolutional layers, I added fully connected dense layers with 256 and 512 units, using the ReLU activation function.

To mitigate overfitting, I implemented dropout layers with a dropout rate of 0.5, which randomly deactivates connections during training to enhance generalization.

Regularization Techniques:

L2 regularization was applied to the dense layers to discourage large weight magnitudes and improve the model's ability to generalize.

I experimented with different regularization strengths, adjusting the regularization factor from 0.01 to 0.001.

Optimizer Configuration:

The Adam optimizer was used with a custom learning rate (e.g., 0.0001) to fine-tune the training process and improve convergence behavior.

Model Compilation:

The model was compiled using the sparse_categorical_crossentropy loss function, suitable for multi-class classification, with accuracy as the primary evaluation metric.

Data Augmentation and Pre-trained Model Exploration:

To address the challenge of a limited dataset, I applied various image augmentation techniques using the Augmentor library. These included rotations, flips, zooming, and random distortions.

In later stages, I experimented with more aggressive augmentations such as blurring and random erasing to further improve the model’s robustness to input variability.

Training and Validation Setup:

Multiple training-validation split ratios were tested before finalizing an 80/20 split.

Augmented data was used during training to increase data diversity, reduce overfitting, and enhance model performance.

3. Conclusion
Through iterative refinement and experimentation, I developed a custom CNN model which surpasses ResNet-50 in terms of classification accuracy on the given dataset.
