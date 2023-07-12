# Skin-Cancer-Detection
## Skin Cancer Detection with Metadata using deeplearning techniques   
***  
### Introduction   
***
According to WHO percentage of people who got effected by skin cancer is increased
to 33% in 2021.Back in 2021, Around 1.2 million people died due to skin cancer all
around world. Where 7.22 lakhs of people are men and 4.76 lakhs of people are
women. Skin cancer is affecting a lot of people from Australia, New Zealand and
Denmark than compared with other countries. Where as in India, most skin cancer
cases are affecting from North India. When human body is exposed to UV rays for
longer time then Basal cells in our humans get affected which is the main cause for
skin cancer and these cells damage the unaffected and active ones which increases the
damage percentage. Generally, Basal cells produce new skin cells when old skin
cells are damaged. But when the skin is affected by skin cancer the Basal cells will
not work properly and will not generate new skin cells. Sooner or later the cancer will
spread throughout the body as there are no new cells produced, which is very dangerous and may lead to death.

Dermoscopy is an assistant diagnosis method which is done by taking some
pictures with the help of computer systems. We used Deep Learning techniques
instead of Machine learning because in ML it takes just a small amount of dataset but
when it comes for classification it requires more data. And even it takes more time for
training the train set to perform as good as dl but still it cannot give us promising and
accurate results. But here comes deep learning which will overcome all the problems
in ml by using neural network. These neural networks are similar to the neurons
in our brain. In dl we can extract the features from the given input and dl can even
take large amount data for train and we can expect efficient accuracy and results. Now
a days, Deep learning became common approach for image detection. It is widely
used for classification and prediction type of problem. Moreover, a greater accuracy
rate of 97.78% was obtained in when the number of layers in CNN was increased
to 14 layers on dermoscopic images from the ISIC dataset.

In previous research papers, They used CNN for processing the image and
later to get better improvements in accuracy they used 5 models for better image classification and for improvement of accuracy in the models of one of the model is Efficient Net B4 which takes less parameters and provides less accuracy we also have
other types of models like Efficient Net B5 which takes less parameters and give us
better accuracy than Efficient Net B4 so in this paper we used Efficient Net B5 as one
of the model in the 5 models which we used.

In our paper, we used CNN instead of ANN because ANN works as human brain
by taking weights. If it anything gets wrong it goes back and gets updates its weights
and again it will work as human brain. The updating of weights is based on cost func-
tion. Where as in CNN, it just uses layers for filtration and analyses the image input.
The layers that are used in CNN are Convolution, ReLU, Pooling, flattening. In our
paper used different types of CNN models like ResNet, GoogleNet, VGGNet, EfficientNet-B5 but found better accuracy for EfficientNet-B5.   
***
### Use of Metadata
***
While there are many CNN models to detect skin cancer but the problem is the prediction of new image with skin cancer. In these models, we used metadata processing.
When it comes to metadata, it has patient records like age, gender, location of infection, diagnosis of cancer, type of skin cancer to patient etc. We used some standard datasets like HAM10000 and ISIC 2019.   
![image](https://github.com/Pavan9303/Skin-Cancer-Detection-/assets/98643288/434a369f-38bb-4bd4-9520-e2df1a33fa36)   
**Fig. 1.** Working of MetaBlock in which we can see that it is the addition of CNN with
Metadata.   
In Fig. 1 it describes the meta block which is our model which contains image data
which is preprocessed, reshaped into a NumPy array and is stored in variable ‘x’ from
the picture we can observe that it also contains metadata which contains records of
patients along with target variable (skin cancer classifier) and we have taken target
variable as ‘y’ which we later categorized into different categories based on skin cancer types in their respective datasets. And used x and y to train and test the CNN model. The overall process will happen inside MetaBlock.    
- Initially imported the dataset from Kaggle and downloaded.
- And Used Label encoder to label the data in the target variable which is in
metadata(CSV file).
- We resized the image data and converted them into NumPy arrays.
- Next we reshaped the NumPy array by dividing them with 255.
- Then we categorized the target variable into 2D array based on number of classes.
- Later we aggregated features of the image along with target variable.
- Then we applied CNN model, GoogleNet, VGGNet, RESNet, EfficientNet-B5 to the aggregated features.  Finally compared the accuracies for all architectures.

