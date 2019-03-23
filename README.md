# Program #2
Easton Tuttle

COSC 4735

Description: Use the Floating Action button in the bottom right-hand corner of the application to take a photo.
After taking a photo, a marker should appear on the map with a smaller version of that photo. Click on the marker
to open a full size version of the photo. Click the "Close Image" button in the top left corner of the application
to close the photo. Repeat as many times as desired.

Google Pixel 2 | 5-inch screen with a 1920x1080 resolution | Android version 9.0

Anything that doesn't work: The application does not survive orientation changes.

# Graded: 47/50 #

* Last location updates are handled when the camera is opened, which creates issues with marker placement when pictures are cancelled. *(-3 points)*

**For example:**

**Test Case:**
Open app at the Engineering Building. Open the camera, but do not take a picture and back out of the camera. Walk over to the Union, take a picture. Walk to the Ben Franklin statue and take a picture

**Result:**
Picture at the Union shows as though it was taken at Engineering and picture of the Ben Franklin statue shows as though it was taken at the Union.

While it may seem intuitive to only get a location when it is needed (i.e. when you want to take a picture and place a marker), it is best just to recieve a constant stream of updating locations on a set interval. Alternatively, you just need to ensure that you are handling the case that no picture is taken. For some reason it still wants to use a location even if you are updating it again the next time you open the camera.

Overall, everything works perfectly if you are only testing for the ideal use case (i.e. everytime the user opens the camera you assume that a picture is taken), but it is important to account for any strange things the user might do when using the app. These are the weird sort of things I will be looking at when testing your apps.
