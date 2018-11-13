Assignments for course Special Topics - RBE 595: Deep Learning For Advanced Robot Perception at Worcester Polytechnic Institute

## Support Vector Machines - Week 1

Implementing a Support Vector Machine based linear image classifier for the CIFAR-10 dataset using Stochastic Gradient Descent optimization. The dataset has 50000 images for 10 classes of images (car, cat, deer, frog, ...)

### Usage

* Download the dataset by running `./getdataset.sh` shell script in _SVM-Week1/f16RBE595/data_ 
* Run the `SVM.py` python script to obtain results.

PS - The shell script might not run unless the privileges are correct and it is declared as an executable(Linux)

### Results

As expected, due to poor resolution of the images(32 X 32 X 3) and this being a very naive implementation of the algorithm, the results obtained were not very good.

* Training Accuracy: ~0.38
* Testing Accuraccy: ~0.41

The final template generated by the weight matrix for all the classes shown below indicates a few classes like car, horse, truck and frog resemble a general representation satisfactorily while other class templates are  not very clear. 

![alt text](https://github.com/kumar-akshay324/dl-assignments/raw/master/SVM-Week1/results/SVM_results_CIFAR-10.png "Final Template Generated from weights")

![alt text](https://github.com/kumar-akshay324/dl-assignments/raw/master/SVM-Week1/results/loss_iters.png "Variation in Loss over the several iterations")


## Image Parser - Week 6

Generate an intermediate dataset by parsing the XML annotation files for given VOC PASCAL 2012 image dataset. The parser extracts subimages from the JPEGImages folder using the annotations provided in the dataset. [here](http://host.robots.ox.ac.uk/pascal/VOC/voc2012/#devkit)

### Usage

* Launch the gen_int_dataset.py python file from within the src/ folder. Uncomment the line #114 to run the complete parser 
* The VOC Dataset should be downloaded and stored one folder above the python script, i.e. in the same folder as the src/ folder. 
* The final generated dataset will be stored in this same folder with the name classes/. The classes folder will have another 20 individual folders representing the 20 classes and store the corresponding images. 

* A binary will also be generated for the images using the _Pickle_ library  in Python. Storing the image information in a serialized manner shall help make its usage in ML applications easier. Generated binary should have the name p_dataset.pkl

### File Structure


```├── Image-parser-Week6
	└── src
	└── VOCdevkit	
	└── classes
	    ├── aeroplane
	    └── cat
	    ..
	    ..
	    ..
	    └── car
```

### Results

* All the images parsed to subimages and stored within individual class folder have been resized to 224 x 224 pixel resolution with restored quality

## Multi-Layer Perceptron and Convolutional Neural Networks for MNIST Handwritten Digit recognition - Week 7

Create an basic MLP neural network and another CNN to classify handwritten digits from the MNIST data available by default through the Keras library. 

### Usage

* Run the _mlp_mnist_data.py_ and _cnn_mnist_data.py_ to execute the MLP and CNN implementation of image classification.
* The MNIST dataset should be automatically downloaded from the keras remote
* Modify the various other hyperparameters in the code.

### File Structure
```
├── cnn-mlp-MNIST-Week7
	├── DL_AKSHAY_KUMAR_HW4.pdf
	├── README.md
	└── src
	    ├── cnn_mnist_data.py
	    └── mlp_mnist_data.py
```

### Results

* MLP Results

Epoch 20/20
60000/60000 [==============================] - 5s 83us/step - loss: 0.0217 - acc: 0.9945 - val_loss: 0.0515 - val_acc: 0.9909
MLP Error: 0.94%

* CNN Results

Epoch 10/10
60000/60000 [==============================] - 131s 2ms/step - loss: 0.0201 - acc: 0.9946 - val_loss: 0.0311 - val_acc: 0.9911
CNN Error: 0.96%


## Face Recognition Using Deep Learning - Week 10

### STILL UNDER HEAVY DEVELOPMENT

### Usage

#### Video to Image Extraction
	* Place the video of the person inside face-recognition-Homework-7-8/videos folder with the name <person_name>.mp4
	* From the main directory of the project, i.e. face-recognition-Homework-7-8/, run `make run`
	* The extracted images should be stored at face-recognition-Homework-7-8/images/<person_name>/image_<frame_number>

### File Structure

### Results

