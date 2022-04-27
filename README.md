# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:

## Developed By: SAFA
## Register Number: 212220230040

### i) Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img=cv2.imread("guit.jpg")
input_img=cv2.cvtColor(input_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
rows,cols,dim=input_img.shape
M=np.float32([[1,0,20],
             [0,1,50],
             [0,0,1]])
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_img)
plt.show()
```
### ii) Image Scaling
```
M=np.float32([[1.5,0,0],
             [0,2,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()

```
### iii) Image shearing
```
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.4,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```
### iv) Image Reflection
```
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()

```
### v) Image Rotation
```
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()

```
### vi) Image Cropping
```
cropped_img=input_img[100:300,100:300]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()

```
## Output:
### i)Image Translation

![5A](https://user-images.githubusercontent.com/75234912/165503814-a91083ec-787e-48d5-a26b-4b48304cbcfe.png)

### ii) Image Scaling

![5B](https://user-images.githubusercontent.com/75234912/165503820-27d4b5e8-7d65-4ff3-84cf-0aac164a4432.png)


### iii)Image shearing

![5C](https://user-images.githubusercontent.com/75234912/165503830-ff8a9b72-8033-460b-9b60-2d1df4d1f8df.png)



### iv)Image Reflection

![5D](https://user-images.githubusercontent.com/75234912/165503843-e5184d5e-47d0-493f-9f28-6f9c32ecfe29.png)



### v)Image Rotation

![5E](https://user-images.githubusercontent.com/75234912/165503853-7b752617-64d7-48a2-b0cf-38653dc587aa.png)

### vi)Image Cropping

![5F](https://user-images.githubusercontent.com/75234912/165503861-cce19a44-a333-4f33-b909-4514a61d821a.png)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
