# COLOR_CONVERSIONS_OF-IMAGE
## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By: HARISH RAGAVENDRA S
### Register Number: 212222230045


## PROGRAM:

### i)Read and Display an Image

```
import cv2
import numpy as np
image_path = 'passport photo.jpg'  
image = cv2.imread(image_path)

if image is None:
   print("Error: Image not found!")
else:
   image = cv2.resize(image,(300,500))
   cv2.imshow("image.my.jpg", image)
   cv2.waitKey(0)
```

### ii)Draw Shapes and Add Text

```
# Draw a line from the top-left to the bottom-right of the image
cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255, 0, 0), 3)

# Draw a circle at the center of the image
center = (image.shape[1]//2, image.shape[0]//2)
cv2.circle(image, center, 50, (0, 255, 0), 3)

# Draw a rectangle around a specific region of interest (ROI)
cv2.rectangle(image, (100, 100), (200, 200), (0, 0, 255), 3)

# Add text at the top-left corner of the image
cv2.putText(image, 'OpenCV Drawing', (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 2)

# Display the modified image
cv2.imshow('Image with Shapes and Text', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### iii)Image Color Conversion
```
# Convert and display the image in different color spaces
# RGB to HSV
hsv_image = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
cv2.imshow('HSV Image', hsv_image)
cv2.waitKey(0)

# RGB to GRAY
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
cv2.imshow('Gray Image', gray_image)
cv2.waitKey(0)

# RGB to YCrCb
ycrcb_image = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('YCrCb Image', ycrcb_image)
cv2.waitKey(0)

# Convert HSV image back to RGB
hsv_to_rgb_image = cv2.cvtColor(hsv_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV to RGB Image', hsv_to_rgb_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### iv)Access and Manipulate Image Pixels
```
# Access and print pixel value at (100, 100)
pixel_value = image[100, 100]
print(f'Pixel value at (100, 100): {pixel_value}')

# Modify the pixel value at (200, 200) to white
image[200, 200] = [255, 255, 255]

# Display the modified image with pixel changes
cv2.imshow('Modified Pixel Image', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### v)Image Resizing
```
# Resize the original image to half its size
resized_image = cv2.resize(image, (image.shape[1]//2, image.shape[0]//2))

# Display the resized image
cv2.imshow('Resized Image', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### vi)Image Cropping

```
# Crop a region of interest (ROI)
roi = image[250:350, 250:350]  # Cropping a 100x100 pixel area starting at (250, 250)

# Display the cropped ROI
cv2.imshow('Cropped ROI', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### vii)Image Flipping
```
# Flip the image horizontally
horizontally_flipped = cv2.flip(image, 1)
cv2.imshow('Horizontally Flipped Image', horizontally_flipped)
cv2.waitKey(0)

# Flip the image vertically
vertically_flipped = cv2.flip(image, 0)
cv2.imshow('Vertically Flipped Image', vertically_flipped)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

### viii)Write and Save the Modified Image
```
# Save the final modified image to your local directory
cv2.imwrite('modified_image.jpg', image)
```

## OUTPUT:

### i)Read and Display an Image
![image](https://github.com/user-attachments/assets/898bb5f7-4cc2-4ee9-b392-90aa4b108dde)
### ii)Draw Shapes and Add Text
![image](https://github.com/user-attachments/assets/f13a7f16-0fd3-4295-a7d1-9dee6b8ea7cd)
### iii)Image Color Conversion
![image](https://github.com/user-attachments/assets/a707451e-54d2-41d4-919d-02f1ab22d9ce)
![image](https://github.com/user-attachments/assets/8a0d98f5-dc72-4308-bead-6f03002b14f2)
![image](https://github.com/user-attachments/assets/7619feac-1fad-4728-b6c9-9ae984226675)
![image](https://github.com/user-attachments/assets/412795c2-9711-4c69-b068-1e35410c8f52)
### iv)Access and Manipulate Image Pixels
![image](https://github.com/user-attachments/assets/2c6dfc43-be08-45ee-93a0-47635a6c527b)
### v)Image Resizing
![image](https://github.com/user-attachments/assets/31e0663e-ef5d-4f48-9137-45b2f05bc6eb)
### vi)Image Cropping
![image](https://github.com/user-attachments/assets/5fd083fd-79b2-400c-a192-edfb71d9cb74)
### vii)Image Flipping
![image](https://github.com/user-attachments/assets/273878b0-8f74-4fee-9617-d94468499e30)
![image](https://github.com/user-attachments/assets/adb50a7f-0e1b-4444-b3fe-bf17dc9dc41e)
### viii)Write and Save the Modified Image
![image](https://github.com/user-attachments/assets/e3098d4f-6de9-4a8f-a1a3-33b6a3b58098)
## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program
