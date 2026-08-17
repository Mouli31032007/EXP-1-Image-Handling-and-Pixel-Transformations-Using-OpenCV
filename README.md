# EXP-1-Image-Handling-and-Pixel-Transformations-Using-OpenCV
# Name: Moulidharan S
# Reg no: 212224240095
Image-Handling-and-Pixel-Transformations-Using-OpenCV
### AIM:
Write a Python program using OpenCV that performs the following tasks:

Read and Display an Image.
Adjust the brightness of an image.
Modify the image contrast.
Generate a third image using bitwise operations.
### Software Required:
Anaconda - Python 3.7
Jupyter Notebook (for interactive development and execution)
### Algorithm:
Step 1:
Load an image from your local directory and display it.

Step 2:
Create a matrix of ones (with data type float64) to adjust brightness.

Step 3:
Create brighter and darker images by adding and subtracting the matrix from the original image.
Display the original, brighter, and darker images.

Step 4:
Modify the image contrast by creating two higher contrast images using scaling factors of 1.1 and 1.2 (without overflow fix).
Display the original, lower contrast, and higher contrast images.

Step 5:
Split the image (boy.jpg) into B, G, R components and display the channels



Ex. No. 01
1. Read the image ('Eagle_in_Flight.jpg') using OpenCV imread() as a grayscale image.
```
import cv2
import matplotlib.pyplot as plt
img = cv2.imread('fly.png', cv2.IMREAD_COLOR)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
plt.imshow(img_rgb, cmap='viridis')  # You can change 'viridis' to another cmap or use None for RGB images
plt.title("Original Image")
plt.axis('off') 
plt.show()
```
2. Print the image width, height & Channel.
```
image = cv2.imread('fly.png')
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape
```
3. Display the image using matplotlib imshow().
```
line_img = cv2.line(img_rgb, (0, 0), (768, 600), (255, 0, 0), 10)
plt.imshow(line_img, cmap='viridis')  
plt.title("Image with Line")
plt.axis('off')  
plt.show()
```
4. Save the image as a PNG file using OpenCV imwrite().
```
image = cv2.imread('fly.png') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
img_rgb.shape



```
5. Read the saved image above as a color image using cv2.cvtColor().
```
circle_img = cv2.circle(img_rgb,(100,150),100,(255,0,0),10)
plt.imshow(circle_img, cmap='viridis')  
plt.title("Image with Circle")
plt.axis('off')  
plt.show()


```
6. Display the Colour image using matplotlib imshow() & Print the image width, height & channel.
```
image = cv2.imread('fly.png') 
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
text_img = cv2.putText(img_rgb, "OpenCV Drawing butterfly", (10, 30), cv2.FONT_HERSHEY_SIMPLEX, 1, (255, 255, 255), 10) 
plt.imshow(text_img, cmap='viridis')  
plt.title("Image with Text")
plt.axis('off')  
plt.show()


```
7. Crop the image to extract any specific (Eagle alone) object from the image.
```
image = cv2.imread('fly.png')
mage_rgb = cv2.cvtCoilor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original RGB Image")
plt.axis("off")



```
8. Resize the image up by a factor of 2x.
```
image_hsv = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2HSV)
plt.imshow(image_hsv)
plt.title("HSV Image")
plt.axis("off")



```
9. Flip the cropped/resized image horizontally.
```
image_gray = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2GRAY)
plt.imshow(image_gray, cmap='gray')
plt.title("Grayscale Image")
plt.axis("off")


```
10. Read in the image ('Apollo-11-launch.jpg').
```
image_ycrcb = cv2.cvtColor(image_rgb, cv2.COLOR_RGB2YCrCb)
plt.imshow(image_ycrcb)
plt.title("YCrCb Image")
plt.axis("off")


```
11. Add the following text to the dark area at the bottom of the image (centered on the image):
```
image_hsv_to_rgb = cv2.cvtColor(image_hsv, cv2.COLOR_HSV2RGB)
plt.imshow(image_hsv_to_rgb)
plt.title("HSV to RGB Image")
plt.axis("off")




```
12. Draw a magenta rectangle that encompasses the launch tower and the rocket.
```
image[100:300, 100:300] = [255, 255, 255] 
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Image with 300x300 White Block")
plt.axis("off")
plt.show()



```
13. Display the final annotated image.
```
image = cv2.imread('fly.png')
image.shape


```
14. Read the image ('Boy.jpg').
```
resized_image = cv2.resize(image, (768 // 2, 600 // 2))
resized_image_rgb = cv2.cvtColor(resized_image, cv2.COLOR_BGR2RGB)
resized_image_rgb.shape
plt.imshow(resized_image_rgb)
plt.title("Resized Image (Half Size)")
plt.axis("off")
plt.show()

```
15. Adjust the brightness of the image.
```
image = cv2.imread('fly.png') 
image.shape
roi = image[50:250, 50:250]
roi_rgb = cv2.cvtColor(roi, cv2.COLOR_BGR2RGB)
plt.imshow(roi_rgb)
plt.title("Cropped Region of Interest (ROI)")
plt.axis("off")
plt.show()




```
16. Create brighter and darker images.
```
img_brighter = cv2.add(img, matrix)
img_darker = cv2.subtract(img, matrix)



```
17. Display the images (Original Image, Darker Image, Brighter Image).
```
image = cv2.imread('fly.png') 
flipped_horizontally = cv2.flip(image, 1)
flipped_horizontally_rgb = cv2.cvtColor(flipped_horizontally, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_horizontally_rgb)
plt.title("Flipped Horizontally")
plt.axis("off")


```
18. Modify the image contrast.
```
flipped_vertically = cv2.flip(image, 0)
flipped_vertically_rgb = cv2.cvtColor(flipped_vertically, cv2.COLOR_BGR2RGB)
plt.imshow(flipped_vertically_rgb)
plt.title("Flipped Vertically")
plt.axis("off")



```

### Output:
<img width="677" height="485" alt="image" src="https://github.com/user-attachments/assets/91f54d04-3e13-41e9-b3bc-47a1d91c2a63" />
<img width="702" height="457" alt="image" src="https://github.com/user-attachments/assets/bc26b5ab-125b-4bbf-9fd9-51fa024fabb8" />
<img width="737" height="447" alt="image" src="https://github.com/user-attachments/assets/321e20b3-1b65-4cd5-bce4-341bd5091e46" />
<img width="803" height="463" alt="image" src="https://github.com/user-attachments/assets/dedc940b-1b5a-40df-884e-eb58bca28658" />
<img width="730" height="453" alt="image" src="https://github.com/user-attachments/assets/3ba97126-12a5-49fb-9e8d-4b8472d0b2a5" />
<img width="787" height="466" alt="image" src="https://github.com/user-attachments/assets/b8d74d85-a532-4a62-8a4a-9b28721f2b59" />
<img width="738" height="466" alt="image" src="https://github.com/user-attachments/assets/d6229eae-c403-42ae-9792-ba87b330ea42" />
<img width="670" height="455" alt="image" src="https://github.com/user-attachments/assets/1e7d7eff-b220-4c14-9439-512bf24500e6" />
<img width="717" height="462" alt="image" src="https://github.com/user-attachments/assets/f757f018-da7b-403a-8265-d8ac832e9f2a" />
<img width="797" height="473" alt="image" src="https://github.com/user-attachments/assets/b2fdb9af-82cc-43bc-b907-c8ec5c8a07fa" />
<img width="781" height="481" alt="image" src="https://github.com/user-attachments/assets/269ae5e9-e077-4b68-a7aa-74cc2962a098" />
<img width="812" height="518" alt="image" src="https://github.com/user-attachments/assets/f88b1055-81dc-4ecb-a44c-066793dd7232" />
<img width="673" height="523" alt="image" src="https://github.com/user-attachments/assets/b85ebc09-dfae-46b9-9aa5-fd34692cd908" />
<img width="748" height="480" alt="image" src="https://github.com/user-attachments/assets/2424f1ff-8831-4e85-8b77-641697544ce4" />
<img width="832" height="460" alt="image" src="https://github.com/user-attachments/assets/1b57e121-e9b7-4c29-94b4-dbeb8e8504bc" />




### Result:
Thus, the images were read, displayed, brightness and contrast adjustments were made, and bitwise operations were performed successfully using the Python program.
