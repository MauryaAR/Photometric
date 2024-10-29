**Objective:** We have a set of fabric and color checker images captured from 9 different angles, and our goal is to develop a program that can process these images for 3D rendering. 
This involves several key steps: image cropping, color correction, and ultimately generating albedo image. Currently, we're using **art engine** to achieve the desired outcome. 
This result can be obtained with the 3D rendering process relying on the **Photometric stereo  technique**. 

Here's step-by-step guide to using photometric stereo on fabrics: 

**1. Capture multiple images:**

  Take images with only one light source active at a time. 
  
  Maintain a fixed camera position for all images. 
  
  Ensure consistent exposure settings across all images. 

**2. Preprocess the images:** 

  Correct for any color inconsistencies between images. 
  
  Handle shadows and specularities, which can be problematic for photometric stereo. 


**3. Apply the photometric stereo algorithm:** 

  Choose an appropriate reflectance model (BRDF). For many fabrics, a modified Lambertian model might work, but we may need more complex models for shiny fabrics. 
  
  Estimate surface normals using the chosen model and the intensity values from images. 
  
  Reconstruct the depth map from the surface normals. 
  
   

 

 
