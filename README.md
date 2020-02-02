# Refocus stereo images after shooting
My algorithm generates a blur map from the input depth map and the user's depth(s) of interest. The blur map is then used to perform depth-based selective blurring of the input image using a Gaussian kernel, resulting in an output image with image regions lying in depth(s) of user's non-interest blurred (degree of blurring is controlled by a input parameter), thus effectively altering the depth of field of the input image.

This submission, used in conjunction with [my stereo depth map generator](http://www.google.com] may be helpful especially for amateur / casual photographers using entry-level cameras with limited capabilities for altering the depth of field during shooting. A typical use case is portrait photography.

A similar project done by Google, although their depth estimation methodology is different:
http://googleresearch.blogspot.in/2014/04/lens-blur-in-new-google-camera-app.html
