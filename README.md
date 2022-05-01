# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it a image variable.

### Step2:
Translate the image using Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]]) Translated_image=cv2.warpPerspective(org_img,Translation_matrix,(col,row))

### Step3:
Scale the image using Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]]) Scaled_image=cv2.warpPerspective(org_img,Scaling_Matrix,(col,row))

### Step4:
Shear the image using Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]]) Sheared_image=cv2.warpPerspective(org_img,Shearing_matrix,(col2,int(row1.5)))

### Step5:
Reflection of image can be achieved through the code Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]]) Reflected_image_row=cv2.warpPerspective(org_img,Reflection_matrix_row,(col,int(row)))

### Step6:
Rotate the image using Rotation_angle=np.radians(10) Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0], [np.sin(Rotation_angle),np.cos(Rotation_angle),0], [0,0,1]]) Rotated_image=cv2.warpPerspective(org_img,Rotation_matrix,(col,(row)))

### Step7:
Crop the image using cropped_image=org_img[10:350,320:560]

### Step8:
Display all the Transformed images.


## Program:
```python
Developed By: Revathi Dayalan
Register Number: 212221240045

import cv2
import numpy as np
import matplotlib.pyplot as plt
original_img=cv2.imread("image.jpeg")
original_img=cv2.cvtColor(original_img,cv2.COLOR_BGR2RGB)
plt.axis("off")
plt.imshow(original_img)
row,col,dim=original_img.shape

i)Image Translation
Translation_matrix=np.float32([[1,0,120],[0,1,120],[0,0,1]])
Translated_image=cv2.warpPerspective(original_img,Translation_matrix,(col,row))
plt.axis("off")
plt.imshow(Translated_image)

ii) Image Scaling
Scaling_Matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
Scaled_image=cv2.warpPerspective(original_img,Scaling_Matrix,(col,row))
plt.axis("off")
plt.imshow(Scaled_image)

iii)Image Shearing
Shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])
Sheared_image=cv2.warpPerspective(original_img,Shearing_matrix,(col*2,int(row*1.5)))
plt.axis("off")
plt.imshow(Sheared_image)

iv)Image Reflection
Reflection_matrix_col=np.float32([[-1,0,col],[0,1,0],[0,0,1]])
Reflected_image_col=cv2.warpPerspective(original_img,Reflection_matrix_col,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_col)

Reflection_matrix_row=np.float32([[1,0,0],[0,-1,row],[0,0,1]])
Reflected_image_row=cv2.warpPerspective(original_img,Reflection_matrix_row,(col,int(row)))
plt.axis("off")
plt.imshow(Reflected_image_row)

v)Image Rotation
Rotation_angle=np.radians(10)
Rotation_matrix=np.float32([[np.cos(Rotation_angle),-np.sin(Rotation_angle),0],
                                [np.sin(Rotation_angle),np.cos(Rotation_angle),0],
                                [0,0,1]])
Rotated_image=cv2.warpPerspective(original_img,Rotation_matrix,(col,(row)))
plt.axis("off")
plt.imshow(Rotated_image)

vi)Image Cropping
cropped_image=original_img[10:350,320:560]
plt.axis("off")
plt.imshow(cropped_image)


```
## Output:
### i)Image Translation

![o2](https://user-images.githubusercontent.com/96000574/166145653-9d531e88-3b79-4f48-a0b2-0f69c16fa1dc.PNG)

<br>
<br>
<br>
<br>

### ii) Image Scaling

![o1](https://user-images.githubusercontent.com/96000574/166145627-339ecd20-5cb4-41bb-9dc8-ee357cc4d93e.PNG)

<br>
<br>
<br>
<br>


### iii)Image shearing
![o7](https://user-images.githubusercontent.com/96000574/166145825-5e6b0abd-5ce2-4beb-83c7-72f7349575eb.PNG)


<br>
<br>
<br>
<br>


### iv)Image Reflection

![o5](https://user-images.githubusercontent.com/96000574/166145613-614a5dd6-ae66-4115-951c-9e3d54195cf7.PNG)
![o6](https://user-images.githubusercontent.com/96000574/166145691-49838d2c-67bb-432d-bfdb-409d8ed2b60e.PNG)

<br>
<br>
<br>
<br>



### v)Image Rotation

![o3](https://user-images.githubusercontent.com/96000574/166145852-30fe88ce-fd62-454c-9231-5de38e5abb44.PNG)

<br>
<br>
<br>
<br>



### vi)Image Cropping

![o8](https://user-images.githubusercontent.com/96000574/166145583-55c39a0b-0665-4cf3-86c3-c3f392e2bdcd.PNG)

<br>
<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
