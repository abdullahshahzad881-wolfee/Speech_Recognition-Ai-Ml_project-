The main objective of this project is to design and develop an Applied Machine Learning (AML) system that can automatically identify these emotions from audio signals. Adding emotion-aware features to applications can significantly improve multiple fields, including healthcare, customer support, security, and human–computer interaction, by making systems more responsive and human-like.
However, recognizing emotions from speech is challenging because human emotions are subtle, complex, and vary across individuals, cultures, and speaking styles. To address these challenges, this project uses deep learning-based models capable of learning both the static patterns and dynamic changes in speech that represent emotional states.
This approach aims to build an accurate, reliable, and practical emotion recognition model suitable for real-world applications.
Deep Learning Architecture
The system utilizes a Convolutional Neural Network (CNN), which excels at extracting spatial patterns from spectrograms, such as identifying key frequency bands. For superior accuracy in complex emotional landscapes, Hybrid Models combining the strengths of CNNs and Recurrent Neural Networks (RNNs)—which capture temporal dependencies—can also be used
•	Conv1D Layer (64 filters, kernel size 5, ReLU activation)
Extracts local patterns from the MFCC input, such as short-term frequency changes in speech.
•	Batch Normalization
Normalizes the output of the previous layer to stabilize learning and speed up training.
•	MaxPooling1D (pool size 2)
Reduces the size of the feature map, helping the model focus on the most important information while lowering computation.
•	Dropout (rate 0.3)
Randomly drops some neurons during training to reduce overfitting and improve generalization.
•	Conv1D Layer (128 filters, kernel size 5, ReLU activation)
Learns deeper and more abstract features that represent complex emotional patterns in speech.
•	Flatten Layer
Converts the 2D feature map into a 1D vector so it can be passed to fully connected layers.
•	Dense Layer (128 units, ReLU activation)
Acts as a fully connected layer that combines learned features and prepares them for classification.
•	Dropout (rate 0.4)
Provides additional regularization to prevent the model from memorizing the training data.
•	Dense Output Layer (Softmax activation)
Produces the final probability distribution across emotion classes, enabling multi-class emotion classification.
