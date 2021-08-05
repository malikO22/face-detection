# face-detection
import cv2
 print ("Package Imported")
 cap=cv2.VideoCapture (0) # to use cam 
while cap.isOpened (): # while loop to dedct faces _, img = cap.read()
 face_cascade =
 cv2.CascadeClassifier ("haarcascade)  frontalface default., xml")
 gray = cv2.cvtColor (img, cv2.COLOR BGR2GRAY) 
Faces = face_cascade.detectMultiscale (gray, 1.1, 4) 
for (x, y, w, h) in Faces:
 cv2.  rectangle (img, (x, y), (x+w, y+h), (255, 0,0),3) 
Cv2.imshow ("image", img) 
if cv2.waitKey (1) & OXFF ==  ord('q'): 
break
 cap.release()
