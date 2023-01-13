# cellfinder
### This script will take the cellfinder summary.csv file for your GFP and tdTomato signal channales, and create a pandas df that shows you the percent cells labled in GFP compared to the percent of cells labled in tdTomato (control) for all brain regions.

# How to use this script 
## step 1
### change the path to your cellfinder output summary.csv path, for poth gfp and tdTomato channels 
#### gfp_df = pd.read_csv("/path/to/your/datas/gfp_summary.csv")
#### tdTomato_df = pd.read_csv("/path/to/your/datas/tdTomato_summary.csv")

## step 2
### change the path variable to where you want this csv file to be saved locally 
#### path = '/path/to/where/you/want/output csv/saved to/
