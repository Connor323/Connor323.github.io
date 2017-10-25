---
title: "Project: Cancer Cell Tracking"
collection: publication_
permalink: /publication/Cancer_Cell_Tracking
excerpt: 'This project focuses on tracking cancer cell based on [**Li et al.**](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2846554/), which used watershed algorithm to segment cells and built a feature vector for cell tracking including the information of position, shape, spatial distribution and texture.'
date: 2016-12-24

---
This project focuses on cell tracking based on [Li et al.](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2846554/). By utilizing watershed algorithm and feature vectors (based on position, shape, spatial distribution and texture), the algorithm can succeed tracking cancer cells in image sequence with segmentation accuracy and tracking accuracy 69.51% and 76.78%, repectively.

## Usage
1. The data can be found at [Cell Tracking Challenge Website](http://www.codesolorzano.com/Challenges/CTC/Datasets.html). 

2. ipython notebook: to better show the algorithm step by step, besides the python scipts, I also create a ipython notebook to visualize the interim results.

3. Some explanation of the scripts:

	**main.py**: the main procedure including all steps.

	**adaptivethresh.py**: compute adaptive thresholding of image sequence in order to generate binary image for Nuclei segmentation.

	**gvf.py**: compute gradient vector field (GVF) to find the seeds for following watershed.

	**watershed.py**: segment cells

	**graph_construction.py**: generate a neighboring graph contraction using Delaunary Triangulation.

	**matching.py**: calculate feature vector for each cell and match cells. 


## Results
1. Result of original image sequence. 

![ ](/images/nomolizedimg.gif "Result of original image sequence")
----

2. Result of tracking all cells. 

![ ](/images/enhance_images.gif "Result of tracking all cells")
----

3. Result of tracking specific cell in mitosis. 

![ ](/images/mitosis_final.gif "Result of tracking specific cell in mitosis")
----

4. Plot of the previous tracking. 

![ ](/images/plotimg.gif "Plot of tracking the mitosis cell")

---
Looking for code? Here is the [link](https://github.com/Connor323/Cancer-Cell-Tracking) to the repository in my Github. 