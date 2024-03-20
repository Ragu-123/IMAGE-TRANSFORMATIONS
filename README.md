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
Display the modified image output.

### Step5:
End the program.

## Program:
```python
Developed By:RAGUNATH R
Register Number:212222240081
```
```
i)Image Translation

import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image=cv2.imread("duck.jpeg")
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("duck.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```


iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("duck.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```


iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("duck.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```



v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("duck.jpeg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),(np.cos(angle)),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image, M, (int(cols),int(rows)))
plt.imshow(rotated_img)
plt.show()
```



vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("duck.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()
```

## Output:
### i)Image Translation
![image](https://github.com/Ragu-123/IMAGE-TRANSFORMATIONS/assets/113915622/e33a3dab-1fa9-47fe-87e1-ceb997f4b234)


### ii) Image Scaling
![image](https://github.com/Ragu-123/IMAGE-TRANSFORMATIONS/assets/113915622/713ac154-2e0c-48df-a3ae-875a6ee36169)


### iii)Image shearing
![image](https://github.com/Ragu-123/IMAGE-TRANSFORMATIONS/assets/113915622/ce9891d5-1926-4933-adfa-6be62b835dba)
![image](https://github.com/Ragu-123/IMAGE-TRANSFORMATIONS/assets/113915622/579fa50c-b150-432b-81ae-62afee655b24)
![image](https://github.com/Ragu-123/IMAGE-TRANSFORMATIONS/assets/113915622/4864a0c2-2bc5-47af-970d-ac5bf8089434)




### iv)Image Reflection
![image](https://github.com/Ragu-123/IMAGE-TRANSFORMATIONS/assets/113915622/785c0512-df22-4162-ad06-20a5c6c91317)
![image](https://github.com/Ragu-123/IMAGE-TRANSFORMATIONS/assets/113915622/d348b79e-0d94-4f56-82ec-76c863c9acea)
![image](https://github.com/Ragu-123/IMAGE-TRANSFORMATIONS/assets/113915622/010995d9-2b73-41ac-a696-52b71a6d66f7)




### v)Image Rotation
![image](https://github.com/Ragu-123/IMAGE-TRANSFORMATIONS/assets/113915622/832f3bee-cfdc-4f51-81e4-f5b38654112b)




### vi)Image Cropping
![image](https://github.com/Ragu-123/IMAGE-TRANSFORMATIONS/assets/113915622/fdf547c3-83a6-442b-a5b3-3732ec9b3c64)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
