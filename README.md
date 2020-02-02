# Refocus stereo images after shooting
My algorithm generates a blur map from the input depth map and the user's depth(s) of interest. The blur map is then used to perform depth-based selective blurring of the input image using a Gaussian kernel, resulting in an output image with image regions lying in depth(s) of user's non-interest blurred (degree of blurring is controlled by a input parameter), thus effectively altering the depth of field of the input image.

This submission, used in conjunction with [my stereo depth map generator](https://github.com/subhayanmukherjee/sparsestereo) may be helpful especially for amateur / casual photographers using entry-level cameras with limited capabilities for altering the depth of field during shooting. A typical use case is portrait photography.

A similar project done by Google, although their depth estimation methodology is different:
http://googleresearch.blogspot.in/2014/04/lens-blur-in-new-google-camera-app.html

Please cite the below [paper](https://doi.org/10.1007/s13319-014-0014-7) if you use the code in its original or modified form:

*S. Mukherjee and R. M. R. Guddeti, “Depth-Based Selective Blurring in Stereo Images Using Accelerated Framework,” 3D Research, vol. 5, no. 3, Jun. 2014.*

# Guidelines

1. Download all files to the same folder.

2. To run the algorithm on the provided input image and depth map, execute the following MATLAB command and see the output:
	imshow(depth_blur('cam_left.jpeg', 'cam_depth_left.png', [10:90], 10))

3. You can also see the provided output image 'output.png' to make sure that my code is working fine on your computer.

4. To perform depth-based blurring for your own (rectified stereo) images, use this submission along with [my stereo depth map generator](https://github.com/subhayanmukherjee/sparsestereo).
