# Face-Emotion-Detection-using-OpenCV-and-DeepFace

Library Imports:
cv2 is imported from OpenCV for image processing.
DeepFace is imported to leverage its functionalities for facial analysis, including emotion detection.

Loading Haar Cascade Classifier:
face_cascade is initialized with a pre-trained Haar cascade classifier for face detection provided by OpenCV.

Loading and Preprocessing Image:
The path to the image file is specified in image_path.
The image is loaded using cv2.imread() into the img variable.
The image is converted to grayscale using cv2.cvtColor() to improve face detection accuracy.

Face Detection:
face_cascade.detectMultiScale() is used to detect faces in the grayscale image.
Detected faces' coordinates (x, y, width, height) are stored in the faces variable.

Face Region Extraction and Emotion Detection:
For each detected face, the code iterates through the faces list.
It extracts the Region of Interest (ROI), i.e., the face area, from the grayscale image using array slicing (face_roi = gray[y:y + h, x:x + w]).
DeepFace's analyze() function is called to perform emotion detection on the extracted face region (face_roi). The region parameter specifies the coordinates of the face for more accurate analysis.
The predicted emotions for the face are stored in the emotions variable.

Display and Visualization:
For each detected face, a rectangle is drawn around it using cv2.rectangle() to mark the face area on the original image (img).
The predicted emotions for each face are printed to the console.



Finally, the image with the detected faces and their respective emotions is displayed using cv2.imshow().

User Interaction:
cv2.waitKey(0) waits for a keyboard event (in this case, 0 implies waiting indefinitely until a key is pressed).
cv2.destroyAllWindows() closes all OpenCV windows once the user presses any key.
This code effectively combines OpenCV for face detection and DeepFace for emotion recognition, allowing you to detect faces in an image, extract face regions, predict emotions for those faces, and visualize the results by marking the faces and their corresponding emotions on the original image.




https://github.com/AnuragNagare/Face-Emotion-Detection-using-OpenCV-and-DeepFace/assets/85473989/253d2493-6b34-4d0d-997b-46f035d116ef


