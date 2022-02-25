# Cellpose notebook for segmenting brightfield images

## Getting started
First, follow the instructions at https://github.com/MouseLand/cellpose#system-requirements to install cellpose and jupyter.
Other than cellpose, the other packages required by the notebook are below:
- matplotlib
- scikit-image

## Accessing the prediction notebook from your laptop
In Terminal, navigate to where you want the code to live. Then, type the following line and press Enter:
`git clone https://github.com/superresolusian/cellpose.git`
The files inside this repository should then be with you. In Terminal, while still in this directory, then type in `jupyter notebook` and a browser window with the current directory's file structure should then open. Click on `run_pretrained.ipynb` and you're good to go!

## Using the notebook
There is only one bit of code that you need to check before running the notebook, which is in the second cell. This is where you tell the code where your images are and where you want to save them.
Once you're happy with that, then go to Kernel > Restart & run all in the jupyter menu. You should get some output printed at the bottom which will let you know how everything's progressing.

## Outputs
I've set up the notebook to output the following into the save directory specified in the code: png files of the masks and outputs (useful for quick visual evaluation), seg.npy file of the segmentation results which can be reloaded into cellpose at a later date, should you wish, and a txt file with outlines that can be loaded as ImageJ ROIs.
To load the outlines into ImageJ, paste the code from https://github.com/MouseLand/cellpose/blob/master/imagej_roi_converter.py into a new macro in ImageJ, set the language to Python, and run the macro.
