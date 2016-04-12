DNA from fecal immunochemical test can replace stool for microbiota-based colorectal
=======

**Background:** There is a significant demand for colorectal cancer (CRC) screening methods that are noninvasive, inexpensive, and capable of accurately detecting early stage tumors. It has been shown that models based on the gut microbiota can complement the fecal occult blood test and fecal immunochemical test (FIT). However, a barrier to microbiota-based screening is the need to collect and store a patient's stool sample.   
**Methods:** Using stool samples collected from 404 patients we tested whether the residual buffer containing resuspended feces in FIT cartridges could be used in place of intact stool samples.  
**Results:** We found that the bacterial DNA isolated from FIT cartridges largely recapitulated the community structure and membership of patients' stool microbiota and that the abundance of bacteria associated with CRC were conserved. We also found that models for detecting CRC that were generated using bacterial abundances from FIT cartridges were equally predictive as models generated using bacterial abundances from stool.  
**Conclusions:** These findings demonstrate the potential for using residual buffer from FIT cartridges in place of stool for microbiota-based screening for CRC. This may reduce the need to collect and process separate stool samples and may facilitate combining FIT and microbiota-based biomarkers into a single test. Additionally, FIT cartridges could constitute a novel data source for studying the role of the microbiome in cancer and other diseases.

Overview
--------

    project
    |- README          # the top level description of content
    |
    |- scratch/	 # for intermediate/temporary files generated while running mothur
    |  |- fit.accnos # list of FIT cartridge samples
    |  |- stool.accnos # list of stool samples
    |  |- fit.files # input file for make.contigs
    |
    |
    |- data/            # data generated from running mothur
    |  |- fit.final.an.unique_list.0.03.cons.taxonomy #consensus classification of OTUs
    |  |- fit.final.an.unique_list.0.03.subsample.0.03.filter.shared #filtered shared file
    |  |- fit.final.an.unique_list.0.03.subsample.shared #subsampled shared file
    |  |- fit.final.an.unique_list.shared #raw shared file
    |  |- fit.final.an.unique_list.sharedsobs.0.03.lt.ave.dist #average number of OTUs shared between samples
    |  |- fit.final.an.unique_list.thetayc.0.03.lt.ave.dist #average thetayc distances between samples
    |  |- fit.final.tx.1.cons.taxonomy #consensus classification for phylotypes
    |  |- fit.final.tx.1.subsample.shared #subsampled phylotype (genus) shared file
    |  |- fit.final.tx.shared #raw phylotype (genus) shared file
    |  |- fit.otus.tax #simplified OTU consensus classification
    |  |- fit.phyla.tax #phylum classification for each genus (for figure 2)
    |  |- fit_only.an.shared #shared file with only FIT cartridges
    |  |- fit_only.an.thetayc.0.03.lt.ave.dist #inter-FIT thetayc distances
    |  |- fit_only.an.thetayc.0.03.lt.ave.mantel #mantel test results
    |  |- metadata.tsv #metadata for all samples
    |  |- stool.an.shared #shared file with only stool samples
    |  |- stool.an.thetayc.0.03.lt.ave.dist #inter-stool thetayc distances
    |
    |- code/           # any programmatic code
    |  |- mothur.batch	# mothur commands for sequence curation
    |  |- mothur.pbs	# PBS script for running mothur.batch
    |  |- cluster1.batch # cluster.split command for distance calculations
    |  |- cluster1.pbs	# PBS script for running cluster1.batch
	|  |- cluster2.batch # cluster.split command for clustering into OTUs
    |  |- cluster2.pbs	# PBS script for running cluster2.batch
    |  |- post_cluster.batch # make.shared, and beta-diversity calculations
    |  |- post_cluster.pbs # PBS script for running post_cluster.batch
    |  |- trimTax.py	# creates a simplified version of the OTU consenus taxonomy file
    |
    |- results         # contains all of the figures
    |
    |- Baxter_FITs_2016.Rmd       # executable Rmarkdown for this study, if applicable
    |- Baxter_FITs_2016.docx      # docx rendered version of the Rmd file
    |- Baxter_FITs_BMCcancer_2016.docx	# cleaned up version of the final manuscript
    |
    |- bmc.csl	# citation style guide for BioMed Central
    |- manuscript_format.docx	# reference document for formatting docx made from Rmd
    |- references.bibtex	# bibtex formatted bibliography for the manuscript
    |
    +- analysis_workflow.md        # step-by-step instructions for processing data
