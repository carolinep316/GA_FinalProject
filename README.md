# GA_FinalProject

I work in single cell RNA sequencing, specifically using the 10X Single Cell product (10X is the name of the company that made the reagent kits we use). For my final project I will be using a dataset that I have used at work.

Quick background on the process: Individual cells are isolated from a sample, and the RNA within each individual cell is barcoded with a molecular identifier (which will be later used to demultiplex our sequencing reads on an individual cellular level). Once the RNA is uniquely tagged they are all pooled back together, and the RNA molecules are reverse-transcribed into cDNA. The DNA libraries are amplified and cleaned up, and tagged with another molecular identifier called a p7 sample index (this will be used to demultiplex on the sample-level), and eventually sequenced.  DNA sequencers use fluorescent-tagged nucleic acids to read each DNA base in our molecule. Out of the sequencers we get raw BCL files, which are massive files that contain the sequences of all of your thousands of reads. 

Downstream analysis pipelines first convert BCLs into fastqs, in which our DNA reads are demultiplexed into each individual sample (using those p7 sample indices mentioned above). The reads are then aligned to a reference genome, and using this reference the pipeline can convert our raw sequences into already-known gene sequences (so we now know what genes are detected in our samples).  Then, using the cellular molecular indices, the pipeline further demultiplexes each sample into every individual cell that comprises that sample. In the end (after about 100 hours of computing time), we end up with a gene-count matrix, in which each cell is represented as a column, and each gene detected is represented in a row. The contents of the matrix represents how many gene counts were detected in each cell.  It is this gene-count matrix that is used for further manual analysis.

(I will have a few slides & diagrams in my final presentation to better illustrate this since I know it's confusing!)

Recently we have run a validation experiment for one of our new single cell products, and I followed a Python tutorial to analyze the data.  For my project, I will expand on this tutorial to answer scientific questions, such as classifying the types of cells in our sample, as well as which genes are the highest detected/most variable for each cell type.

If you would like to see the tutorial, as well as the code I used, see the notebooks I uploaded to this repository.
