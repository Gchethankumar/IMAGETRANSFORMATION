# IMAGE TRANSFORMATION

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
Display the modified image output.

### Step5:
End the program.

## Program:
```
Developed By: G.Chethan Kumar
Register Number: 212222240022
```
### i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("dodge.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(in_img)
plt.show()
```
### ii) Image Scaling
```python
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("dodge.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1,0,100],
              [0,1,100],
              [0,0,1]])
trans_img=cv2.warpPerspective(in_img, M, (cols,rows))
plt.axis('off')
plt.imshow(trans_img)
plt.show() 
```
### iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("dodge.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()
```
### iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("dodge.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,  0,0  ],
                [0,-1,rows],
                [0,0,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0  ],
                [ 0,0,1  ]])
reflect_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  
```
### v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("dodge.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()  
```
### vi)Image Cropping

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("dodge.jpg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[10:290 ,10:360]
plt.imshow(cropped_img)
plt.show()
```

## Output:

### i)Image Translation

![Screenshot from 2023-09-13 21-29-02](https://github.com/Gchethankumar/IMAGETRANSFORMATION/assets/118348224/62e8deae-df95-4da6-9efb-feb653eb44c1)


### ii) Image Scaling

![Screenshot from 2023-09-13 21-29-06](https://github.com/Gchethankumar/IMAGETRANSFORMATION/assets/118348224/f5ff2792-8bc9-4e06-82db-cd0664b0e4e7)


### iii)Image shearing

![Screenshot from 2023-09-13 21-29-19](https://github.com/Gchethankumar/IMAGETRANSFORMATION/assets/118348224/9040a260-88c3-48e1-9f83-74dcb936f06f)


### iv)Image Reflection

![Screenshot from 2023-09-13 21-29-24](https://github.com/Gchethankumar/IMAGETRANSFORMATION/assets/118348224/0c0b397f-1abf-4f5d-a784-2cb4ae7f2aed)


### v)Image Rotation

![Screenshot from 2023-09-13 21-29-31](https://github.com/Gchethankumar/IMAGETRANSFORMATION/assets/118348224/566599fe-83d4-4e8d-aefe-de4351ac9138)


### vi)Image Cropping

![Screenshot from 2023-09-13 21-29-49](https://github.com/Gchethankumar/IMAGETRANSFORMATION/assets/118348224/f0df36b4-bca8-49ca-93b7-858c57e8fbbf)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
