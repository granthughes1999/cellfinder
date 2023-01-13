# cellfinder
#### If your running this from the Denman Lab Neuropixel Aquisition Computer skip Step 1
#### These are the steps for running the open source cellfinder package on Estim collected lightsheet images

## Step 1
### Create an Anaconda enviroment
#### open Anaconda prompt
##### >> conda create -n cellfinder python=3.9
##### >> conda activate cellfinder
##### >> pip install cellfinder

## step 2
#### Edit the batch file in this repository in the following way to match your data
#### line 4: conda call (your cellfinder env name)
#### line 6: Update all 6 varaibles (-s, -b, -o, --orentation, -v, --atlas)
##### -s path/to/signal/channel (directory path to .tif photos of gfp channel)
##### -s path/to/second-signal/channel (directory path to .tif photos of tdTomato channel)
##### -b path/to/autoflourecent/channel (directory path to .tif photos of autoflourecent/background channel)
##### -o path/to/where you want/cellfinder output files to save to/ 
##### --orentation Three letters representing orenation of your .tiff images (example: spl)
##### -v voxel spacing 

# Step 2
#### Open Anaconda prompt
#### Drag and drop the updated batch file in this repository into the anaconda prompt


### This script will take the cellfinder summary.csv file for your GFP and tdTomato signal channales, and create a pandas df that shows you the percent cells labled in GFP compared to the percent of cells labled in tdTomato (control) for all brain regions.

# How to use this script 
## step 1
### change the path to your cellfinder output summary.csv path, for poth gfp and tdTomato channels 
#### gfp_df = pd.read_csv("/path/to/your/datas/gfp_summary.csv")
#### tdTomato_df = pd.read_csv("/path/to/your/datas/tdTomato_summary.csv")

## step 2
### change the path variable to where you want this csv file to be saved locally 
#### path = '/path/to/where/you/want/output csv/saved to/
