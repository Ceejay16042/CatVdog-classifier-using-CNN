# CatVdog-classifier-using-CNN
A Cat vs dog classifier system built using transfer learning in CNN
## During the phase of this project, the following operations were carried out:

- Data sourcing from !wget --no-check-certificate \
    "https://download.microsoft.com/download/3/E/1/3E1C3F21-ECDB-4869-8368-6DEBA77B919F/kagglecatsanddogs_5340.zip" \
    -O "/tmp/cats-and-dogs.zip"

- Extraction of the dataset, which is in a zip format, into the /tmp folder.
- Splitting the cats and dogs images into training and validation datasets using the copyfile method in the shutil module with a 90:10 ratio for training and testing.
- Specifying the file paths to the various images (cats and dogs) using the path.join method in the os module.
- Visualization of dog and cat images using Matplotlib.
- Applying transfer learning by instantiating the INCEPTION V3 class which is an image recognition model that has proven to attain more than a 78.1% accuracy on ImageNet dataset.
- Freezing the weights of the layers in the image recognition model to make them untrainable, thereby allowing the addition of extra layers to be added to the model for improved training and validation accuracy.
- Applying the dropout method by randomly dropping 20% of the neurons in the neural network for regularization of the model and to prevent overfitting.
- Fitting the dataset to the model and running a training cycle for 15 epochs.
- Model evaluation resulted in a training score of 91% and a validation score of 96%
- Testing the model on several dog and cat images resulted in accurate labeling of the images belonging to cats and dogs.
