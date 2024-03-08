# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages.
<br>
### Step2:
Load the image file in the program.
<br>

### Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
<br>

### Step4:
Display the modified image output.
<br>

### Step5:
End the program.
<br>

## Program:
```python
Developed By: VINOD KUMAR S
Register Number: 212222240116
```
```python
i)Image Translation
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread( "car.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis( 'off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,100],
               [0,1,100],
               [0,0,1]])
translated_image =cv2.warpPerspective(input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("timesquare.jpg")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```


iii)Image shearing

``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("sphere.jpg")
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

iv)Image Reflection
``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("statue.jpg")
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


v)Image Rotation


``` python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("photograph.jpg")
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

vi)Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("beach.jpg")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[2000:3000 ,1000:2500]
plt.imshow(cropped_img)
plt.show()
```

## Output:

### ORINGINAL IMAGE:
![originalimg](https://github.com/vinodkumar-s/IMAGE-TRANSFORMATIONS/assets/113497226/4595d5eb-f6db-4818-8f1f-fd5013f5a394)

### i)Image Translation

![transform](https://github.com/vinodkumar-s/IMAGE-TRANSFORMATIONS/assets/113497226/d245bd2d-5114-4e38-8fe6-0c1c3d135942)


### ii) Image Scaling
![Screenshot 2024-03-08 153222](https://github.com/vinodkumar-s/IMAGE-TRANSFORMATIONS/assets/113497226/4eca9649-368f-46c6-8d43-f1299a6a403f)


### iii)Image shearing
![Screenshot 2024-03-08 153328](https://github.com/vinodkumar-s/IMAGE-TRANSFORMATIONS/assets/113497226/ad6daa22-a4f5-49b9-9354-638e5fd1e6a0)
![Screenshot 2024-03-08 153338](https://github.com/vinodkumar-s/IMAGE-TRANSFORMATIONS/assets/113497226/9d92d8de-b3e4-4c4a-97eb-0964e4476004)



### iv)Image Reflection

![Screenshot 2024-03-08 153501](https://github.com/vinodkumar-s/IMAGE-TRANSFORMATIONS/assets/113497226/8d7de3c2-7521-4421-b4cd-3863136c7abf)
![Screenshot 2024-03-08 153517](https://github.com/vinodkumar-s/IMAGE-TRANSFORMATIONS/assets/113497226/38897a8b-cdc3-4738-a58c-68ae718b8885)


### v)Image Rotation
![Screenshot 2024-03-08 153603](https://github.com/vinodkumar-s/IMAGE-TRANSFORMATIONS/assets/113497226/3a6b192f-545e-49de-bada-f8eb6dd20437)


### vi)Image Cropping
![Screenshot 2024-03-08 153619](https://github.com/vinodkumar-s/IMAGE-TRANSFORMATIONS/assets/113497226/fa793f64-7883-4858-84e4-d8b9b7da8362)




## Result:
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
