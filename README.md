<h1>Pneumonia Detection Deep Neural Network Model</h1>
<h2>Aim: </h2>
<h2>Pneumonia, an inflammatory condition of the lungs, is a leading cause of morbidity and mortality worldwide. Early and accurate diagnosis is crucial for effective treatment and better patient outcomes. Traditional methods for diagnosing pneumonia, such as chest X-rays, rely heavily on the expertise of radiologists, which can lead to variability in interpretation and potential delays in diagnosis. To address these challenges, this project aims to develop a robust Pneumonia Detection algorithm leveraging deep learning techniques.</h2>

<h2>About Pneumonia: </h2>
<h2>Pneumonia is a lung infection that makes it hard to breathe. It can be caused by bacteria, viruses, or fungi. When someone has pneumonia, the tiny air sacs in their lungs fill with fluid, causing symptoms like coughing, fever, chills, and difficulty breathing.
Anyone can get pneumonia, but it is more dangerous for very young children, elderly people, and those with other health problems. Doctors use chest X-rays and other tests to diagnose pneumonia and usually treat it with medications to fight the infection. Early treatment is important to avoid serious complications.</h2>

<h2>Step-by-step procedure: </h2>
<h2>Dataset: </h2>
<h2>I have used a Chest X-Ray dataset from <a href="https://www.kaggle.com/">Kaggle</a> (link at the end of this subpoint). There are 5856 Chest X-Ray examples in the dataset. The dataset is already split into train, cross-validation and test set. However, the main problem with the predefined split is that instead of a standard split of 70-15-15 , the validation set was around 0.27% of the dataset. Training a neural network with this split would give very bad results no matter what hyperparameter tuning or regularization I do. So, ultimately I did my own split of 70-20-10 on the dataset with a distribution of about 70% images for Pneumonia Positive and 30% for Pneumonia Negative.
Dataset Link: <a href="https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia">Pneumonia Dataset</a>.</h2>

<h2>Data Preprocessing: </h2>
<h2>I have applied simple data augmentation to the different splits. The images were horizontally rotated along with shearing and zooming. I also normalized the pixels to limit their values from -1 to 1 by simply dividing each pixel value by 255 (The max value). Another detail to be noted is that the colour mode while augmentation was taken as Grayscale. An image X-Ray can be easily represented as a Grayscale image; this also reduces unnecessary computations as it lowers the image dimensions from (64 X 64 X 3) to (64 X 64 X 1).</h2>

<h2>Convolutional Neural Networks: </h2>
<h2>A Convolutional Neural Network (CNN) is a type of deep learning algorithm specifically designed for processing and analyzing visual data. CNNs are widely used in image recognition, computer vision, and various other tasks involving visual inputs due to their ability to automatically and adaptively learn spatial hierarchies of features from images. There networks are built by comprising convolutional layers as the main computational units. The main advantage of such layers is that they greatly reduce the number of parameters to be trained while efficiently capturing image features. 
