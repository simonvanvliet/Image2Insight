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


conda env export --from-history > name


ml Java/11.0.3_7

conda create -n delta2_env cudnn=8 cudatoolkit=11 python=3.9

conda activate delta2_env

export LD_LIBRARY_PATH="$CONDA_PREFIX/lib/"

pip install delta2

 

Setting the LD_LIBRARY_PATH is necessary every time after you've activated this conda env, for example in your slurm scripts. I'm not sure if it's necessary during the build of the conda env as I'm not sure how delta2 is built. But doesn't hurt to set it after building CUDA etc in case the packages are looking for it. Also, the sub shell on the compute nodes sometimes doesn't initialize conda properly so I recommend including the following hook in your slurm script before your conda activate command eg:

 

eval "$(conda shell.bash hook)"

conda activate delta2_env

export LD_LIBRARY_PATH="$CONDA_PREFIX/lib/"

python ...

 