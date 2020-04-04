# Background Remover using Tiramisu 

Background Remover is built using Tiramisu, State-of-the-art approaches for semantic image segmentation built on 100 layers Convolutional Neural Networks (CNNs), and trained using CamVid datasets. Model was trained using Laptop with NVidia GPU and is designed to remove background of an image using semantic image segmentation.

# Dataset used for training the model

Used CamVid dataset with 32 classes and the dataset was developed by Alex Kendall. It is available at the following repo: https://github.com/alexgkendall/SegNet-Tutorial/tree/master/CamVid


CamVid dataset is very apt for semantic segmentation because it provides annotations needed for context generation and segmentation. Data is divided into training (and trainannot), test (and testannot), and val (and valannot). 

# Using Pretrained model to perform background removal

To see the performance of model based on Tiramisu, I had used pretrained Semantic Image Segmentation pretrained models from Google called DeepLab. For more information on DeepLab, please go to following: https://github.com/tensorflow/models/tree/master/research/deeplab

I had used the following pretrained model: <b>deeplabv3_mnv2_pascal_train_aug</b>

![Image of DeepLab](https://github.com/anigasan/GCI/blob/master/bgremover/images/deeplab.png)

# Results

Overall both the models are performing good with the images with different backgrounds and in different contexts. 

| Original Image       | Tiramisu based          | Deep Lab Model |    Comments |
| ------------- |:-------------:| -----:|-----:|
| ![Image of Halo jump](https://github.com/anigasan/GCI/blob/master/bgremover/images/halo.jpeg)    | ![image of Halo](https://github.com/anigasan/GCI/blob/master/bgremover/images/halo.png) | ![image of Halo](https://github.com/anigasan/GCI/blob/master/bgremover/images/halo%20(1).png) | Both the models are performing on par. Some of the details like Tom Cruise's forearm is missing in both the sgemented images  |
| ![Image of Halo jump](https://github.com/anigasan/GCI/blob/master/bgremover/images/dwayne.jpg)    | ![image of Halo](https://github.com/anigasan/GCI/blob/master/bgremover/images/dwayne.png) | ![image of Halo](https://github.com/anigasan/GCI/blob/master/bgremover/images/dwayne.png) | Both the models are performing on par with tiny portions of background retained  |
| ![Image of Halo jump](https://github.com/anigasan/GCI/blob/master/bgremover/images/tom1.jpg)    | ![image of Halo](https://github.com/anigasan/GCI/blob/master/bgremover/images/tom12.png) | ![image of Halo](https://github.com/anigasan/GCI/blob/master/bgremover/images/tom1%20(1).png) | Surprisingly Tiramisu based model had lost some of the detail that DeepLab Model had retained  |
| ![Image of Halo jump](https://github.com/anigasan/GCI/blob/master/bgremover/images/beyonce2.jpg)    | ![image of Halo](https://github.com/anigasan/GCI/blob/master/bgremover/images/beyonce2.png ) | ![image of Halo](https://github.com/anigasan/GCI/blob/master/bgremover/images/beyonce3.png) | There is some loss to background in Tirumisu model  |
| ![Image of Halo jump](https://github.com/anigasan/GCI/blob/master/bgremover/images/Yoda1.jpeg)    | ![image of Halo](https://github.com/anigasan/GCI/blob/master/bgremover/images/Yoda1.png) | ![image of Halo](https://github.com/anigasan/GCI/blob/master/bgremover/images/Yoda1.png) | Looks like either of the models had not worked  with Yoda's background! Force is too strong, you say???!!  |
