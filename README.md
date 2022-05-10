# CamVid-Cambridge-Driving-Labeled-Video-Database-Image-Segmentation
## - by Gangesh Vaniyamkandi

### Introduction:
Perform Image segmentation on Cambridge-Driving Dataset

The Cambridge-driving Labeled Video Database (CamVid) provides ground truth labels that associate each pixel with one of 32 semantic classes. This dataset is often used in (real-time) semantic segmentation research.

We have an image and a its mask with the segmentation of classes as shown below:

![image-](https://user-images.githubusercontent.com/66409831/167540309-f19829d5-7a60-45b5-9d5e-0f0ddbfb9f81.png)  ![mask](https://user-images.githubusercontent.com/66409831/167540369-d3266e88-49b5-49d1-a7a6-25baa34778dc.png)

The dataset is split up as follows:

601 training pairs
100 test pairs

I have used pretrained segmentation models with U-Net as the artitechture and trained two models with one with RestNet34 and other with VGG16 as the backbone.

Performance Metric used is IOU Score and the loss function used is Dice loss.

With the Resnet34 i have got a IOU score of 0.3979 and with the VGG16 model the IOU score is 0.4637.

But when we compare the predicted test images for both the models the RestNet34 model image segmentation looks better than the VGG16 model.

Below are some Sample Test image segmentation genetrated using both the models.







For the complete code please check out the ipynb.

