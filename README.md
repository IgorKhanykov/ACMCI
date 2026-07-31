# ACMCI
Agglomerative Clustering Method for Color Images (ACMCI) - a solution for generalizing the Arifin-Asano agglomerative clustering method to the case of a color image by introducing an ordering of elementary color clusters and a system of actions for reducing the dimensionality of "big data".

07/31/2026, 15:24, RF, Saint Petersburg, SUAI, Engineering School, Machine Learning Laboratory, a423 

The repository now contains the first results of agglomerative cluster processing of color images, obtained during debug runs of a MATLAB program developed by the author. The program fully executed according to the developed algorithm, generating the entire specified series of partitions: the full portion of the accelerated calculations stage and the full portion of the exact calculations stage.
"Accelerated calculations" means that the program pairwise merges all consecutive clusters without calculating the "minimal pair."
"Exact calculations" means that the software algorithm searched for the "minimal pair" (the pair with the minimum value of the intercluster distance function) among the obtained set of pairs at each iteration of the loop.

Note: The obtained results are preliminary, as the program did not achieve the control value for a cluster count of 1 (the approximation error is higher than the control value). However, the results demonstrate the success of the software-algorithmic approach to reducing the number of calculations, allowing for approximate partitions, albeit not precisely, to be obtained, which with conventional agglomerative calculations would require 2^47 iterations of loops to process arrays of 256^3 cells.

Time costs for processing standart color Lena, 512x512, image is about 900 seconds. Color image 4-1-07 "Jelly Beans 1", 256x256 - about 90 seconds. Color image wash-ir "Washington, D.C." (infra-red) - about 14000 seconds. Image "Aurora Borealis", 3008 - about 24000 sec.
The calculations were performed on a home laptop manufactured in 2014. 

Field of sciences: intersection of image processing and unsupervised learning.
Task: color image segmentation, multiple partitions.
Task execution technique: cluster analysis.

Sources of preceseed images:
<https://sipi.usc.edu/database/>;
<https://en.wikipedia.org/wiki/Aurora>;
<>



Igor Khanykov


