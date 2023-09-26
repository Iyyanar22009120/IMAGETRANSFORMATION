# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

### Step1: 
Import numpy,cv2,matplotlib.pypolt packages.
### Step2:
Load the image file in the program.
### Step3:
Use the Translation,Scaling,Shearing,Reflection,Rotation,Cropping using OpenCV and Python.
### Step4:
Display the modified image output.
### Step5:
End the program.

## Program:
```
Developed By:IYYANAR S
Register Number:212222240036
```
## reading the original image
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
plt.imshow(img)
plt.show()
```
i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
rows,cols,dim=img.shape
M=np.float32([[1,0,-250],
              [0,1,250],
              [0,0,1]])
trans=cv2.warpPerspective(img, M, (cols,rows))
plt.axis('off')
plt.imshow(trans)
plt.show() 
```

ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
rows,cols,dim=img.shape
M=np.float32([[1.5,0,0],
              [0,1.3,0],
              [0,0,1]])
scaled=cv2.warpPerspective(img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled)
plt.show()  
```


iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
rows,cols,dim=img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()
```


iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
rows,cols,dim=img.shape
M_x=np.float32([[1, 0,0   ],
                [0,-1,rows],
                [0, 0 ,1  ]])
M_y=np.float32([[-1,0,cols],
                [ 0,1,0   ],
                [ 0,0,1   ]])
reflect_x=cv2.warpPerspective(img,M_x,(int(cols),int(rows)))
reflect_y=cv2.warpPerspective(img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflect_x)
plt.show()
plt.axis('off')
plt.imshow(reflect_y)
plt.show()  
```



v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
rows,cols,dim=img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()     
```



vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
img = cv2.imread("blue.jpg")
img = cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
cropped_img=img[200:500,800:1100]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### reading the image
![read5](https://github.com/Iyyanar22009120/IMAGETRANSFORMATION/assets/118680259/e8d0e93d-9250-4c31-84fa-6db2352d9c47)

### i)Image Translation

![translate5](https://github.com/Iyyanar22009120/IMAGETRANSFORMATION/assets/118680259/027b2a8b-ef86-40bf-bc8f-ff05d8135f09)

### ii) Image Scaling

![scaling5](https://github.com/Iyyanar22009120/IMAGETRANSFORMATION/assets/118680259/8a3c0bea-425f-4025-9dc6-8fd27f540805)


### iii)Image shearing
![shearing5](https://github.com/Iyyanar22009120/IMAGETRANSFORMATION/assets/118680259/f2d1e227-e75b-4296-9cb2-8504aacf04fb)



### iv)Image Reflection

![reflection5](https://github.com/Iyyanar22009120/IMAGETRANSFORMATION/assets/118680259/3dcc77e7-1a65-4926-b76c-ecaa5b542fec)



### v)Image Rotation

![rotation5](https://github.com/Iyyanar22009120/IMAGETRANSFORMATION/assets/118680259/77c6689a-89ab-482b-922a-5066c40a87e8)



### vi)Image Cropping
![cropping5](https://github.com/Iyyanar22009120/IMAGETRANSFORMATION/assets/118680259/49c0c705-23bc-417b-8ad9-665a3c5b08c4)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
