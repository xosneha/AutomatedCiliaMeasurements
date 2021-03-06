# AutomatedCiliaMeasurements
Pipeline to measure cilia, cell nucleis, and which cilia are close to which cell nucleis from microscopy images using CellProfiler and Python.

# Components
1) CellProfiler pipeline -- This collects the number of cell nuclei and cilia, as well as where they are in the image (their centres) & their sizes/shapes. It also saves the trace of nuclei/cilia seen in the CP pipeline.

2) Python script centertocenter.py -- This finds out which cilia is closest to which nuclei given the above pipeline, assuming one cell:one cilia ratio and a threshold length away they can be (in pixels). 

3) Python script label_cp_im.py -- This takes saved images of nuclei and cilia from the pipeline, and numbers them based on their centres in order to visualize the pipeline.

4) Python script visualize.py -- This does the same thing as above, but superimposes the cilia numbers on the nuclei pictures and draws a line from the closest cilia to the closest cell to visualize the centertocenter script.  

5) Python script calc.py -- This calculates mean and standard deviation of the columns 'ImageNumber', 'AreaShape_Area', 'AreaShape_MajorAxisLength', and 'AreaShape_MinorAxisLength' for both nuclei and cilia and outputs it as a dictionary.  