# CamVid-Cambridge-Driving-Labeled-Video-Database-Image-Segmentation
## - by Gangesh Vaniyamkandi

---

### Requirements
- NumPy
- Pandas
- OpenCV
- TensorFlow
- Keras
- Mathplotlib
- imgaug
- segmentation_models
---

### Introduction:
Perform Image segmentation on Cambridge-Driving Dataset

The Cambridge-driving Labeled Video Database (CamVid) provides ground truth labels that associate each pixel with one of 32 semantic classes. This dataset is often used in (real-time) semantic segmentation research.

We have an image and a its mask with the segmentation of classes as shown below:

![image-](https://user-images.githubusercontent.com/66409831/167540309-f19829d5-7a60-45b5-9d5e-0f0ddbfb9f81.png)  ![mask](https://user-images.githubusercontent.com/66409831/167540369-d3266e88-49b5-49d1-a7a6-25baa34778dc.png)

The dataset is split up as follows:

601 training pairs
100 test pairs

## Model:

I have used pretrained segmentation models with U-Net as the artitechture and trained two models with one with RestNet34 and other with VGG16 as the backbone.

U-Net is an architecture for semantic segmentation. It consists of a contracting path and an expansive path as shown below:

![unet](https://user-images.githubusercontent.com/66409831/167596022-f906397b-4520-4f7a-a765-415216e8ece6.png)


## Performance Metric used is IOU score:

IOU score is the measures the amount of overlap between the predicted and ground truth bounding box.

![iou](https://user-images.githubusercontent.com/66409831/167600548-c40d0eba-336e-47e8-beb2-e035e56f883f.JPG)


IOU score ranges between 0 and 1, where score 1 is the best case and score 0 the worst case.


## Loss function used is Dice loss:

Range of Loss Function is 0 to 1

Dice Loss is one minus dice coefficient which is also known as Fscore. Where Fscore The F-score (Dice coefficient) can be interpreted as a weighted average of the precision and recall, where an F-score reaches its best value at 1 and worst score at 0.

Dice coefficient measures the overlap of two sets of area and at every iterations moves towards decreasing the dice loss to zero thus increasing the dice coefficient to one, thus creating a perfect segmentation of the image.

## Final Scores:

With the Resnet34 i have got a IOU score of 0.3979 and with the VGG16 model the IOU score is 0.4637.

But when we compare the predicted test images for both the models the RestNet34 model image segmentation looks better than the VGG16 model.

Below are some Sample Test image segmentation genetrated using both the models.

## Test Images:

### restnet34:

![download](https://user-images.githubusercontent.com/66409831/167542939-66c7c142-fc33-478d-8531-339292a573e6.png)

![download2](https://user-images.githubusercontent.com/66409831/167542975-19fdd8e9-099b-4014-a789-13a46d6911a0.png)

![download3](https://user-images.githubusercontent.com/66409831/167542996-e75e92f1-53f2-4c4a-90a4-549023b94244.png)

![download4](https://user-images.githubusercontent.com/66409831/167543027-28c93969-a552-423a-9428-ed8162f1a454.png)

![download5](https://user-images.githubusercontent.com/66409831/167543064-76194a5a-9350-45a1-9369-e52518ac4468.png)

### vgg16:

![download](https://user-images.githubusercontent.com/66409831/167583231-3f49562a-55fa-43a5-a34d-7a6589b722b9.png)

![download1](https://user-images.githubusercontent.com/66409831/167583286-342797c8-61d8-47a3-83fa-8aeb87a0e633.png)

![download2](https://user-images.githubusercontent.com/66409831/167583327-91fd78c6-ba13-4c43-8549-f2fe502aee2d.png)

![download3](https://user-images.githubusercontent.com/66409831/167583376-37e7e488-ab61-4b9e-9a97-99ff1248075f.png)

![download4](https://user-images.githubusercontent.com/66409831/167583416-37f5e8d0-7018-4c8d-9b8a-64cea8d5d012.png)



For the complete code please check out the [ipynb](https://github.com/gangesh404/CamVid-Cambridge-Driving-Labeled-Video-Database-Image-Segmentation/blob/main/CityScapes_Image_Segmentation.ipynb).

