# <p align="center">Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it a image variable.
<br>

### Step2:
Translate the image
<br>

### Step3:
Scale the image
<br>

### Step4:
Shear the image
<br>

### Step5:
Reflection of image
<br>

### Step6:
Rotate the image
<br>

### Step7:
Crop the image
<br>

### Step8:
Display all the Transformed images.
<br>

## Program:
### Developed By: M VIGNESH
### Register Number: 212220233002
```python
i)Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("image.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
cv2.imshow('Input',img)
plt.imshow(img)
cv2.waitKey(0)
plt.axis("on")
rows,cols,dim=img.shape
translation_matrix=np.float32(([1,0,100],[0,1,200],[0,0,1]))
translated_img=cv2.warpPerspective(img,translation_matrix,(cols,rows))
plt.axis("off")
plt.imshow(translated_img)

ii) Image Scaling
scaling_matrix=np.float32([[1.2,0,0],[0,1.2,0],[0,0,1]])
scaled_img=cv2.warpPerspective(img,scaling_matrix,(cols,rows))
plt.axis("off")
plt.imshow(scaled_img)

iii)Image shearing
shearing_matrix=np.float32([[1,0.2,0],[0.2,1,0],[0,0,1]])
sheared_img=cv2.warpPerspective(img,shearing_matrix,(cols*2,int(rows*1.5)))
plt.axis("off")
plt.imshow(sheared_img)

iv)Image Reflection
reflection_matrix_col=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_col=cv2.warpPerspective(img,reflection_matrix_col,(cols,int(rows)))
plt.axis("off")
plt.imshow(reflected_img_col)
reflection_matrix_row=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
reflected_img_row=cv2.warpPerspective(img,reflection_matrix_row,(cols,int(rows)))
plt.axis("off")
plt.imshow(reflected_img_row)

v)Image Rotation
rotation_angle=np.radians(10)
rotation_matrix=np.float32([[np.cos(rotation_angle),-np.sin(rotation_angle),0],
                                [np.sin(rotation_angle),np.cos(rotation_angle),0],
                                [0,0,1]])
rotated_img=cv2.warpPerspective(img,rotation_matrix,(cols,(rows)))
plt.axis("off")
plt.imshow(rotated_img)

vi)Image Cropping
cropped_img=img[10:350,320:560]
plt.axis("off")
plt.imshow(cropped_img))
```
## Output:
### i)Image Translation
![Screenshot (42)](https://user-images.githubusercontent.com/75234588/166111732-f5f9da35-c94b-460e-a0b2-ff0061592208.png)

<br>

![Screenshot (43)](https://user-images.githubusercontent.com/75234588/166112103-8d606d57-b5a8-4f48-9dd4-da470143e19d.png)



# ii) Image Scaling
##![Screenshot (44)](https://user-images.githubusercontent.com/75234588/166111757-860b0dc8-6dd9-499d-8e94-e74806196572.png)

### iii)Image shearing
![Screenshot (45)](https://user-images.githubusercontent.com/75234588/166111783-5175403e-4621-4e79-a8e5-b447bf86175d.png)


### iv)Image Reflection
![Screenshot (49)](https://user-images.githubusercontent.com/75234588/166112077-85264b69-ab6a-49cc-bcb9-9d27f6d3bd6c.png)
<br>
![Screenshot (50)](https://user-images.githubusercontent.com/75234588/166112098-51f310e2-c1a5-449a-a075-19d781d26bff.png)





### v)Image Rotation
![Screenshot (47)](https://user-images.githubusercontent.com/75234588/166111846-350728e8-97db-4cad-8481-37dd5374fa73.png)


### vi)Image Cropping
![Screenshot (48)](https://user-images.githubusercontent.com/75234588/166111852-8dbf873e-d110-4e53-a569-18eacfd0a958.png)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
