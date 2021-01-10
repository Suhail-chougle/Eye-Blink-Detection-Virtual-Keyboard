# Eye-gaze-controlled-keyboard

The project is divided into 4 major steps\
\
(1)Detecting the eyes\
To detect the eyes we we the "dlib" library which in turn uses the landmarks of the face to detect them.\
We then get the coordinates of the eyes and calculate the vertical distance\
\
(2)Detecting if the eyes are blinking\
The idea is if the user blinks then the vertical length of the eye reduces considerably or even zeros down\
For this we use the blinking ratio which is nothing but (horizontal length of the eye/vertical length of the eye)\
We do this for both the eyes and average it\
If this ratio goes beyond a certain threshold we say the user is blinking\
\
(3)To make the virtual keyboard\
We make two sets of keyboard;left and the right side\
\
(4)Detecting where the user is looking(left or right)\
For this we divide each eye into two parts and for an eye if the white part in the right side of the eye is more than the left side we say the user is looking at the left\
Hence we calculate Eye aze ratio for both eyes and average it\
\
With some other small helper functions we link the above steps and get our desired output
