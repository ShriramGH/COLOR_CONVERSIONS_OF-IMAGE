# COLOR_CONVERSIONS_OF-IMAGE

## AIM


#### To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv) To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:

### Anaconda - Python 3.7

## Algorithm:


### Step 1

Choose an image and save it as a filename.jpg 

### Step 2

Use imread(filename, flags) to read the file.


### Step 3

Use imshow(window_name, image) to display the image.

### Step 4

Use imwrite(filename, image) to write the image.

### Step 5

End the program and close the output image windows.


### Step 6

Convert BGR and RGB to HSV and GRAY

### Step 7

Convert HSV to RGB and BGR

### Step 8

Convert RGB and BGR to YCrCb

### Step 9

Split and Merge RGB Image


### Step 10

Split and merge HSV Image

 ```python
Developed By: Shriram S
Register Number: 212222240098
```

#### IMAGE 

![RGB](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/269a64e5-4caa-4b52-a915-6df0e13b616d)


## Program:


### (i) Read and display the image
 ```py
#Read and display the image
import cv2
image=cv2.imread('city.jpg',1)
image=cv2.resize(image,(200,325))
cv2.imshow('Shriram',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Output:

![image](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/8e91e2a3-8621-4fb1-b097-9b6e874c2323)


## Program:

### (ii) Write the image

```py
#Write the image
import cv2
image=cv2.imread('RGB.jpg',0)
cv2.imwrite('demos.jpg',image)
```

### Output

![image](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/9d8bec1b-76d2-4806-9ef8-be428db88f75)


## Program:

### (iii) Shape of the Image

```py
#Shape of the Image
import cv2
image=cv2.imread('RGB.jpg',1)
print(image.shape)
```


### Output

![image](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/380e2ec8-1f29-468c-8000-09229dde6e27)



## Program:

### (iv) Access rows and columns
```py
#Access rows and columns
import random
import cv2
image=cv2.imread('RGB.jpg',1)
image=cv2.resize(image,(400,400))
for i in range (150,200):
    for j in range(image.shape[1]):
        image[i][j]=[random.randint(0,255),
                    random.randint(0,255),
                    random.randint(0,255)] 
cv2.imshow('part image',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```


### Output

![image](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/fd83948c-2722-49d3-900e-6cb358c7d560)



## Program:

### (v) Cut and paste portion of image
```py
#Cut and paste portion of image
import cv2
image=cv2.imread('RGB.jpg',1)
image=cv2.resize(image,(400,400))
tag =image[150:200,110:160]
image[110:160,150:200] = tag
cv2.imshow('partimage1',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output

![image](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/cf98985f-6e05-4c66-b64a-198cf54f31d6)


## Program:

### (vi) BGR and RGB to HSV and GRAY
```py
#BGR and RGB to HSV and GRAY
import cv2
img = cv2.imread('RGB.jpg',1)
img = cv2.resize(img,(300,200))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Original Image

![RGB](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/269a64e5-4caa-4b52-a915-6df0e13b616d)


### Output

![image](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/2ecb0901-44df-4261-86f0-6a60efc31c40)

## Program:

### (vii) HSV to RGB and BGR

```py
#HSV to RGB and BGR
import cv2
img = cv2.imread('RGB.jpg')
img = cv2.resize(img,(300,200))

img = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('Original HSV Image',img)

RGB = cv2.cvtColor(img,cv2.COLOR_HSV2RGB)
cv2.imshow('2HSV2BGR',RGB)

BGR = cv2.cvtColor(img,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',BGR)

cv2.waitKey(0)
cv2.destroyAllWindows()

```
### Original HSV

![image](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/22886fde-8b0d-4df5-bce4-d2c037992475)


### Output


![image](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/723c15d7-3a59-4a0f-91af-6f95e73bb42a)


## Program:

### (viii) RGB and BGR to YCrCb
```py

#RGB and BGR to YCrCb
import cv2
img = cv2.imread('RGB.jpg')
img = cv2.resize(img,(300,200))
cv2.imshow('Original RGB Image',img)

YCrCb1 = cv2.cvtColor(img, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb1)

YCrCb2 = cv2.cvtColor(img, cv2.COLOR_RGB2YCrCb)
cv2.imshow('BGR-2-YCrCb',YCrCb2)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output


![image](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/8913cef9-9b35-42a5-b7a8-1bf0142c6eb8)


## Program:

### (ix) Split and merge RGB Image
```py
#Split and merge RGB Image
import cv2
img = cv2.imread('RGB.jpg',1)
img = cv2.resize(img,(300,200))

R = img[:,:,2]
G = img[:,:,1]
B = img[:,:,0]

cv2.imshow('R-Channel',R)
cv2.imshow('G-Channel',G)
cv2.imshow('B-Channel',B)

merged = cv2.merge((B,G,R))
cv2.imshow('Merged RGB image',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```
### Output

#### Channels

![image](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/51fc27f3-0772-4df7-8f1e-71bece61d555)


#### Merged RGB


![image](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/1ccbafdb-c2ec-4c64-95bd-197e4d43761e)


## Program:

### (x) Split and merge HSV Image
```py
#Split and merge HSV Image
import cv2
img = cv2.imread("RGB.jpg",1)
img = cv2.resize(img,(300,200))
img=cv2.cvtColor(img,cv2.COLOR_RGB2HSV)

H,S,V=cv2.split(img)

cv2.imshow('Hue',H)
cv2.imshow('Saturation',S)
cv2.imshow('Value',V)

merged = cv2.merge((H,S,V))
cv2.imshow('Merged',merged)

cv2.waitKey(0)
cv2.destroyAllWindows()
```

### Output

### Merged HSV


![image](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/0328a881-c148-4b03-ad07-2a1813cb778a)



### Splitted


![image](https://github.com/ShriramGH/COLOR_CONVERSIONS_OF-IMAGE/assets/117991122/cf678218-8f74-468c-9e91-f682856d1035)


## Result:
#### Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







