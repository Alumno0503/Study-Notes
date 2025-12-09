You can find the images in the assignment package “tung_ping_chau_view1.jpeg” and
“tung_ping_chau_view2.jpeg”.The goal of this part of the assignment is to stitch the two images
together.
1. Load the images and convert to grayscale. Explain, in the notebook, why do we want to do so.

2. Use the Harris detector to detect the corner points. Writing your own detector is recommended as good practice, but using the OpenCV library is also fine.

3. Use the OpenCV library to extract keypoints and compute descriptors through the function SIFT_create.detectAndCompute(). Output the number of keypoints in each image.
You can find more details in the OpenCV documents. Note: To be efficient, you may want
to use no more than 5,000 keypoints in this case.

4. Match the keypoints using the BFMatch() function in OpenCV.

5. Compute the homography from the matched points using RANSAC. Print the Homography
Matrix and explain in the notebook how RANSAC works here.

6. Warp “tung_ping_chau_view2.jpeg” onto the other using the estimated transformation.
This can be done with the perspectiveTransform() and warpPerspective() functions in
OpenCV.

7. Create the new image and show the result.