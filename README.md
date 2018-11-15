# Massively parallel profiling of HIV-1 resistance to the fusion inhibitor enfuvirtide 
### Adam S. Dingens, Julie Overbaugh, and Jesse D. Bloom


Experiments analyzed here were performed by Adam Dingens in the [Bloom lab](http://research.fhcrc.org/bloom/en.html) and [Overbaugh lab](https://research.fhcrc.org/overbaugh/en.html) in the late 2017 - 2018.  

Here, we use slightly modified version of mutational antigenic profiling, which we can refer to as resistance profiling, to comprehensively map resistance to `enfuvirtide`, also known as `T-20` and tradename `Fuzeon`. We use BG505.T332N mutant Env libraries, first described and characterized in [Haddox, Dingens et al 2018](https://elifesciences.org/articles/34420). The triplicate mutant libraries used here correspond to the three BG505 replicates in this paper. 

We use [dms_tools2](https://jbloomlab.github.io/dms_tools2/) to analyze the data . This notebook processes the Illumina deep sequencing data, and then analyzes the enfuvirtide selection. 

[Dingens et al 2017](http://dx.doi.org/10.1016/j.chom.2017.05.003) describes mutational antigenic profiling in detail. The barcoded subamplicon Illumina sequencing approach is described [here](https://jbloomlab.github.io/dms_tools2/bcsubamp.html), and the computation of `differential selection` is described [here](https://jbloomlab.github.io/dms_tools2/diffsel.html).


## Organization
The mutational antigenic profiling analysis is performed by the iPython notebook [`analysis_notebook.ipynb`](analysis_notebook.ipynb). 

Subdirectories:

   * `./results/` is generated by [`analysis_notebook.ipynb`](analysis_notebook.ipynb). `./results/` contains the individual directories, each with the outputs from different steps in the analysis, such as the `codoncounts`, `renumbered codon counts`, `fraction surviving`, `fration surviving above average`, and `differential selection` data. For example `./results/diffsel/` contains all of the `differential selection` output, both for individual replicates and summary data. However, the easiest way to get median differential selection measures for enfuvirtide is from from File S2.
   
   * `./results/FASTQ_files/` contains the input Illumina deep sequencing data. This file is generated by [`analysis_notebook.ipynb`](analysis_notebook.ipynb), which downloads the sequencing files from the [Sequence Read Archive](http://www.ncbi.nlm.nih.gov/sra).

   * `./data/` contains all input data needed to run [`analysis_notebook.ipynb`](analysis_notebook.ipynb)). Files are described in the iPython notebok when used. 


## Results and Conclusions
All of the results are breifly detailed in the [`analysis_notebook.ipynb`](analysis_notebook.ipynb) notebook; click on this notebook to see the results.
