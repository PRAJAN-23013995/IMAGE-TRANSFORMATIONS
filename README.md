# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.

### Step2:
Load the image file in the program.

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

### Step4:
Display the modified image output

### Step5:
End the program.

## Program:
```python
Developed By: PRAJAN P
Register Number: 212223240121
i)Image Translation:

import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread("cats.jpeg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
print("PRAJAN P\n 212223240121")
plt.subplot(1, 2, 1)
plt.imshow(input_image)
plt.axis('off')
plt.title("Input Image")
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],[0,1,70],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.subplot(1, 2, 2)
plt.imshow(translated_image)
plt.axis('off')
plt.title("Image Translation")
plt.show()

ii) Image Scaling:

input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
print("PRAJAN P \n212223240121")
plt.subplot(1, 2, 1)
plt.imshow(input_image)
plt.axis('off')
plt.title("Input Image")
rows,cols,dim=input_image.shape
M=np.float32([[1.7,0,0],[0,1.8,0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.subplot(1, 2, 2)
plt.imshow(translated_image)
plt.axis('off')
plt.title("Image Scaling")
plt.show()


iii)Image shearing:

input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
print(" PRAJAN P\n212223240121")
plt.subplot(1, 2, 1)
plt.imshow(input_image)
plt.axis('off')
plt.title("Input Image")
rows,cols,dim=input_image.shape
M1=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M2=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols*1.5),int(rows*1.5)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols*1.5),int(rows*1.5)))
plt.subplot(1, 2, 2)
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.axis('off')
plt.title("Image Shearing")
plt.show()


iv)Image Reflection:

input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
print("PRAJAN P \n212223240121")
plt.subplot(1, 2, 1)
plt.imshow(input_image)
plt.axis('off')
plt.title("Input Image")
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.subplot(1, 2, 2)
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.axis('off')
plt.title("Image Reflection")
plt.show()


v)Image Rotation:
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
print("PRAJAN P \n212223240121")
plt.subplot(1, 2, 1)
plt.imshow(input_image)
plt.axis('off')
plt.title("Input Image")
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.subplot(1, 2, 2)
plt.imshow(translated_image)
plt.axis('off')
plt.title("Image Rotation")
plt.show()




vi)Image Cropping:

h, w, _ = input_image.shape
cropped_face = input_image[int(h*0.2):int(h*0.8), int(w*0.3):int(w*0.7)]
cv2.imwrite("cropped_face.png", cv2.cvtColor(cropped_face, cv2.COLOR_RGB2BGR))
print("PRAJAN P \n212223240121")
plt.figure(figsize=(10,5))
plt.subplot(1, 2, 1)
plt.imshow(input_image)
plt.axis('off')
plt.title("Input Image")
plt.subplot(1, 2, 2)
plt.imshow(cropped_face)  
plt.axis('off')
plt.title("Cropped Image")
plt.show()



```
## Output:
### INPUT IMAGE:

![download](https://github.com/user-attachments/assets/4722fa93-b329-468e-8611-c113d0e86f61)


### i)Image Translation

![download](https://github.com/user-attachments/assets/73978663-9c63-49a5-9e22-fd27fdb6c818)


### ii) Image Scaling

![download](https://github.com/user-attachments/assets/7f53dc06-0931-4a57-8e98-83268181daf4)


### iii)Image shearing

![download](https://github.com/user-attachments/assets/8a7ad2de-dad3-4d57-ac18-1d194c963dca)


### iv)Image Reflection

![download](https://github.com/user-attachments/assets/c90fc49b-15d4-4fbe-b379-09a381da6eb3)


### v)Image Rotation

![download](https://github.com/user-attachments/assets/663306ee-89c4-44ed-afc3-5b917a34a77f)

### vi)Image Cropping

![download](https://github.com/user-attachments/assets/ddd9a10b-5d78-4c8b-94ba-7896a63ad7cf)

## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
