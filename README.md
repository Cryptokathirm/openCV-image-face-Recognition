# openCV-image-face-Recognition
#python OpenCv library
#pip install opencv-python
import cv2

# to detect the face using this xml file
# to link the file in CascadeClassifier function
data = cv2.CascadeClassifier('haarcascade_frontalface_default.xml')
# read the image
img = cv2.imread('facial-recognition-test.jpg', 1)

# detectMultiScale given the coordinates from the image
faces = data.detectMultiScale(img)
print(faces)

# multiple face detect using for loop
for x, y, w, h in faces:
    # rectangle function is detect the face and givin output like a Box
    cv2.rectangle(img, (x, y), (x + w, y + h), (0, 0, 550), 2)
# show the image
cv2.imshow('facial-recognition-test.jpg', img)

# for the window waiting
key = cv2.waitKey(0)


#image link Here
#https://mymodernmet.com/wp/wp-content/uploads/2020/10/facial-recognition-test.jpg
