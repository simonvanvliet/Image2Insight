##  Fiji 

Add the following update sites:
- PTBIOP (not needed)
- Ilastik (not needed)


- Go to `Plugins` -> `Ilastik` -> `Run Pixel Classification Prediction`
Then

Here we will use the Linear Stack Alignment with SIFT MultiChannel plugin
- To install it, add the PTBIOP to your update sites and update Fiji.
- Got to `Plugins` -> `Registration` -> `Linear Stack Alignment with SIFT MultiChannel`
- In the window set the alignment channel to the index of the phase contrast channel (likely 3)
- Increase the maximum offset to 100
- Set initial Gaussian blur to 10pixels