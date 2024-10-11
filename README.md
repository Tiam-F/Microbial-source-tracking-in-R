# Microbial-source-tracking-in-R
Microbial fecal source tracking in R

Files used for microbial fecal source tracking in R. The files are used to process Illumina (short reads) and Nanopore (long reads) data. The data are combined with microbial fecal libraries, which give output files for source tracking (Sourcetracker2). The data can also be visualized using relative abundance. Not all chunks in the code are needed, just use the relevant ones for your requirements.

--- The files aren't completely clean, I'll work on them when I have time.---

* Source_tracking_with_sewageLib.Rmd
Contains a method for extracting and processing water samples with a fecal library. Writes a BIOM file and a metadata file as output to be used in source tracking (Sourcetracker2 in Linux).
Creates a barplot from the output files of source tracking to visualize the match with sewage samples.


* a_b_diversity.Rmd
Plot the alpha and beta diversity of both Illumina and Nanopore data. Create a relative abundance plot for the water samples sequenced with Illumina and Nanopore at different taxonomic levels. A rarefaction curve plot can also be generated, with the option of using rarefied or non-rarefied data. 


* illumina_rarefaction.Rmd
Not in use at the moment.

* mock_illumina_nanopore.Rmd
The relative abundance plot of the mock community (ZymoBIOMICS Catalog No. D6331) sequenced with Illumina and Nanopore at different
taxonomic levels.

* plot_waterSamples.Rmd
PCA/NMDS plots of the water samples with and without the mock community combined. Check and plot certain bacteria of interest.
Spiked water samples (mock spiked) were processed into PCA/NMDS plots.
The water samples were analyzed using the GTDB-curated EMU database and the default database from EMU.

* sourcetracking_cleaned.Rmd
Source tracking preprocessing to create a BIOM file and metadata to be used in the Sourcetracker2 and SourcePredict programs.
(Spiked samples used in plot_waterSamples.Rmd are generated from this file).
