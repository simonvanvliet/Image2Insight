# Setup BACMMAN
BACMMAN (BACteria in Mother Machine Analyzer) is a ImageJ plugin that offers a fully automated workflow to analyze mother machine data.

## Install Fiji
- Download at: https://fiji.sc 
- On Mac/Linux: copy Fiji app to application folder (or other folder of choice)
  - Note: OSX will give a security warning, please go into settings to give permission to launch Fiji
- On Windows: copy Fiji app to a folder in your user space e.g. `C:\Users\[your name]\ImageJ.app`
  
## Already have Fiji installed?
Please install a fresh copy of Fiji nonetheless! You can have multiple copies of Fiji on your computer, simply rename the new copy of Fiji to e.g. Fiji_Bacmman.    

## Update Fiji
- Start Fiji
- Update Fiji with default update sites (ImageJ / Fiji / Java 8)
  - Go to `Help` -> `Update`
  - In ImageJ Updater window click on `Apply Changes`
- Restart Fiji 
- Repeat until message 'Your ImageJ is up to date!' message appears 

## Install Bacmman
- Go to `Help` -> `Update`
- In ImageJ Updater window  click on `Manage update sites`
- In the list select (add a tick to tick box) the following extra update sites:
  - BACMMAN (https://sites.imagej.net/BACMMAN/)
  - BACMMAN-DL (https://sites.imagej.net/BACMMAN-DL/)
  - ImageScience (https://sites.imagej.net/ImageScience/)
- Click `Close`
- In ImageJ Updater window click on `Apply Changes`
- Restart Fiji 

## Test Bacmmann (optional)
- Work trough the tutorial in getting_started_bacmann.md



# BACMMAN Resources
- Detailed protocol (classical algorithm):  https://doi.org/10.1038/s41596-019-0216-9)
- Publication describing Deep Learning algorithm: https://doi.org/10.48550/arXiv.2003.07790
- BACMMAN Wiki: https://github.com/jeanollion/bacmman/wiki
- Tutorial adept configuration: https://github.com/jeanollion/bacmman/wiki/How-to-Adapt-Configuration
