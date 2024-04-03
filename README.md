# MNIST-CNN-Project
This project demonstrates the implementation and evaluation of a Convolutional Neural Network (CNN) on the MNIST dataset, a collection of handwritten digits. The model is built using TensorFlow and Keras libraries, showcasing the entire workflow from data preprocessing to model evaluation.

<h2>Project Structure</h2>

Here's a brief overview of the main files in this repository:

<li>README.md: This file, which documents the project and its usage.</li>
<li>mnist_cnn.py: The Python script that includes the CNN model implementation, training, and evaluation on the MNIST dataset.</li>
<li>requirements.txt: A list of Python dependencies required to run the project.</li>
<li>final_model.h5: The saved model file generated after training (not included in this repo, it will be created when you run mnist_cnn.py).</li>

<h2>Features</h2>
<li>Data Preparation: Reshaping and normalizing the MNIST dataset for CNN processing.</li>
<li>Model Definition: Building a CNN using layers like Conv2D, MaxPooling2D, BatchNormalization, Flatten, and Dense.</li>
<li>Model Training and Evaluation: Employing k-fold cross-validation and early stopping during training.</li>
<li>Visualization: Plotting training and validation loss and accuracy.</li>
<li>Prediction: Demonstrating model predictions on test images.</li>

<h2>Model Architecture</h2>
The CNN model includes the following layers:
<li>Two Conv2D layers with ReLU activation and BatchNormalization.</li>
<li>Two MaxPooling2D layers to reduce spatial dimensions.</li>
<li>Flatten layer to convert 2D features to 1D.</li>
<li>Two Dense layers with ReLU and softmax activation for classification.</li>
  
<h2>Evaluation</h2>
The model is evaluated using k-fold cross-validation to ensure robustness and generalization. The evaluation metrics include accuracy and loss for both training and validation phases.

<h2>Results</h2>

After training, the model achieves an accuracy of 98.9% on the MNIST test dataset.

<img width="819" alt="Screenshot 2024-04-03 at 10 43 43" src="https://github.com/shoneeze/MNIST-CNN-Project/assets/69034556/f24b3f84-5b0e-418e-89f0-c49e56495839">

The confusion matrix provides a visual and quantitative measure of the model's performance across different classes. 
From the matrix:
<li>The model shows strong performance for most digits, with the majority of predictions falling along the diagonal, indicating correct classifications.</li>
<Li>Misclassifications are present but relatively low, with off-diagonal numbers revealing where these occurred. For example, the digit '5' was occasionally mistaken for '3' and '8'.</Li>
<li>The digit '2' was most commonly misclassified as an '8', which happened 10 times, suggesting a visual similarity that the model may confuse.</li>
<li>The digit '5' seems to pose the most challenge to the model, with the lowest count of correct predictions (878) compared to other digits.</li>

<h2>Future Enhancements</h2>
<li>Experiment with different model architectures or hyperparameters to improve accuracy.</li>
<li>Implement additional data augmentation techniques to improve model robustness.</li>
