# Mucosal Deformation Analysis
JupyterLab Notebooks used by the Linden Lab to analyze the mean intensity of ROIs from experiments applying focal deformation to mucosal receptive fields. 

## Installation 
1. Download and Extract Files
2. Open .ipynb files in JupyterLab 

## Usage
Before starting, these notebooks have hardcoded numbers pertaining to our particular experiment that may need to be changed if utilizing a different setup. 

Step 1:
1. We record our videos split in two halves of 28,500 frames each, which means we import two log files each with 28,500 datapoints for 57,000 points total. These numbers will need to be changed if you have a different number of frames in your recording
2. Out experiment deforms the mucosa at 24 different spots. The program splits the data into 24 seperate chunks, so this number may need to change depending on your procedure
3. The timings of the deformation of the mucosa and the start and end of each chunk are hardcoded in the 4th and 5th cells. These will need to be changed to match the timing of your experiment.

Step 2:
1. Similarly to Step 1, there are references to "24 spots" in the code that will need to be changed to fit the parameters of your experiment.
2. The locations of the 24 spots are necessary for graphing responses spatially and will need to be changed. These spots are defined in Cell 2.

Step 1 Usage:
1. Install all dependencies.
2. Cell 20 is a commented out cell that creates a .csv file with the correct formating for usage in both Steps. Uncomment the code, input your desired name for the .csv file after "CSVfileName =", and run the cell by itself to generate your .csv file.
3. Add the name of your .csv file in cell 2 after "CSVfileName =".
4. Restart the kernel and run all cells. You will be prompted to provide 3 files: The first half of the ROI intensity data, the second half of the ROI intensity data, and the location data for the ROIs (Left, Top, Width, Height)
5. Select the GI Region and Plexus of your cells
6. Further analysis will be guided by GUI. 

Step 2 Usage: 
1. Install all dependencies
2. Add the name of your .csv file in cell 3 after "filename =".
3. Restart kernel and run all cells. 

## License
This project is licensed under the [MIT License](LICENSE)
