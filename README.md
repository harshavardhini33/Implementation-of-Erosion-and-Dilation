# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.


### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring image for dilation/erosion

### Step4:
Apply erosion and dilation using cv2.erode and cv2.dilate

### Step5:
Plot the images using plt.imshow

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText
img1=np.zeros((100,660),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(img1,'M.HARSHAVARDHINI',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1,'gray')
plt.axis('off')


# Create the structuring element
kernel=np.ones((5,5),np.uint8)


# Erode the image
image_erode1=cv2.erode(img1,kernel)
plt.imshow(image_erode1,'gray')
plt.axis('off')



# Dilate the image
image_dilatel=cv2.dilate(img1,kernel)
plt.imshow(image_dilatel,'gray')
plt.axis('off')
```
## Output:

### Display the input Image
![download](https://user-images.githubusercontent.com/93427208/169644051-6ffe9a72-04ba-4c6e-8824-22107dc47f30.png)


### Display the Eroded Image
![download](https://user-images.githubusercontent.com/93427208/169644056-f4778352-5b41-413c-bda7-4992229af1a8.png)


### Display the Dilated Image
![download](https://user-images.githubusercontent.com/93427208/169644060-00d0b297-212d-4a91-afd7-1f385c8cc54e.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
