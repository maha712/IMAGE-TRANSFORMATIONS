# IMAGE-TRANSFORMATIONS


## Aim

To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:

Anaconda - Python 3.7

## Algorithm:

### Step1:

Import numpy module as np and pandas as pd.

### Step2:

Assign the values to variables in the program.

### Step3:

Get the values from the user appropriately.

### Step4:

Continue the program by implementing the codes of required topics

### Step5:

Thus the program is executed in google colab.

## Program:

Developed By:mahalakshmi k

Register Number:212222240057
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('masha.webp')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis('off')
```
output

![luffy](https://github.com/user-attachments/assets/621d8d4c-049d-4d3f-ac46-cca38718aed7)

i)Image Translation
```
rows, cols, _ = image.shape
M_translate = np.float32([[1, 0, 50], [0, 1, 100]])  
translated_image = cv2.warpAffine(image_rgb, M_translate, (cols, rows))

plt.imshow(translated_image)
plt.title("Translated Image")
plt.axis('off')
```
output

![luffy2](https://github.com/user-attachments/assets/65e0152d-cf80-400a-aefc-f8620a3647c6)


ii) Image Scaling
```
scaled_image = cv2.resize(image_rgb, None, fx=1.5, fy=1.5, interpolation=cv2.INTER_LINEAR)

plt.imshow(scaled_image)
plt.title("Scaled Image")
plt.axis('off')
```
output

![luffy3](https://github.com/user-attachments/assets/1646ba6d-29cf-4600-9a49-3727aa309adb)

iii)Image shearing
```
M_shear = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  # Shear with factor 0.5
sheared_image = cv2.warpAffine(image_rgb, M_shear, (int(cols * 1.5), int(rows * 1.5)))

plt.imshow(sheared_image)
plt.title("Sheared Image")
plt.axis('off')
```
output
![luffy4](https://github.com/user-attachments/assets/28f83108-8638-4dea-a53c-844ba82cb2e1)



iv)Image Reflection
```
reflected_image = cv2.flip(image_rgb, 1)


plt.imshow(reflected_image)
plt.title("Reflected Image")
plt.axis('off')
```
output
![luffy5](https://github.com/user-attachments/assets/c751d8e5-81e3-434b-b360-3b27c05703f6)


v)Image Rotation
```
M_rotate = cv2.getRotationMatrix2D((cols / 2, rows / 2), 45, 1) 
rotated_image = cv2.warpAffine(image_rgb, M_rotate, (cols, rows))


plt.imshow(rotated_image)
plt.title("Rotated Image")
plt.axis('off')
```
output

![luffy 6](https://github.com/user-attachments/assets/b036ddd2-1dd4-4e03-bbe5-7eede83aa1c8)

vi)Image Cropping
```
cropped_image = image_rgb[50:300, 100:400]
plt.figure(figsize=(12, 8))
plt.tight_layout()
plt.show()

plt.figure(figsize=(4, 4))
plt.imshow(cropped_image)
plt.title("Cropped Image")
plt.axis('off')
plt.show()
```
output

![luffy 7](https://github.com/user-attachments/assets/9d12a6b4-13d7-4689-a097-65f73686333c)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
