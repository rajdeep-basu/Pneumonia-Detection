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
