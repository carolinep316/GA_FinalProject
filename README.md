# GA_FinalProject

I work in genomic science - specifically, single-cell RNA sequencing. 

A very brief summary of what this process looks like: Individual cells are isolated, the DNA within is extracted, and the DNA code is read on a sequencer. Sophisticated pipelines help us deconvolute the DNA sequence and simplify it down to a matrix containing the gene counts within each cell. These matrices can be uploaded to Python or R for additional manual analysis.

For my final project I will be using a dataset that I have used at work.

Recently we ran a validation experiment and I followed a Python tutorial to analyze the data.  The workflow uses clustering to groups similar cells together (based on their genetic code), thereby allowing us to identify and classify different cell types within a sample. For Part I of my project I will walk you through this tutorial. For Part II I use new data from a different experiment and run it through Part I's clustering to compare this new cell type to our previously classified ones. 
