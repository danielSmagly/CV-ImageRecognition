## Computer Vision Image Recognition Project

Using two different image classification deep learning models, trained with the full CIFAR-10 dataset, the goal of the project is to develop an accurate CNN model as well as a CNN model with transfer learning that achieves the best possible classification results.

## Methodology:
For this project, the provided CIFAR-10 dataset only needed a few normalizations  and adjustments before it was sent to the model. Each channel of the image was divided by 255 to bring it into the range of [0, 1], and the y values were on-hot-encoded as this was a classification problem. For the CNN model that utilized transfer learning, further adjustments needed to be made to the image resolution (increase from 32x32 px to 64x64 px) in order for the images to be properly processed.

## Experimental Results and Analysis:
Once the data was ready to be processed into the CNN model, I began with a model that used two Conv2D layers, two MaxPooling layers, three dropout layers and a Dense layer. The input size for the  Conv2D layers started at 32 and was doubled for each following layer. This initial model gave fairly strong early results with an accuracy of about 72%. Further adjustments were made to the amount of Conv2d/MaxPooling/Dropout layers as well as their input size, with the final model iteration resulting in an accuracy of about 80%. The batch size was kept at 64 in order for the model to maintain good performance and reduce chance for RAM overload in Google Colab.

The model utilizing transfer learning resulted in slightly less accurate results, reaching at accuracy of about 70%, although this could be a result of not utilizing the full dataset in order to avoid crashing and overloading the allotted Google colab RAM. This model added one 256 input Dense layer and one 10 output Dense layer on top of the preset layers transferred from the VGG16 model. 
