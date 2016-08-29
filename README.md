# neuro_wave_bergen
Setup for using common neuroimaging software on the wave and bergen servers at Rice.   Inspired by John Muschelli's documentation for the jhpce cluster at Johns Hopkins (https://github.com/muschellij2/neuro_cluster) 

##FSL 

To use [`FSL`](http://fsl.fmrib.ox.ac.uk/fsldownloads/) add the following to your .cshrc profile:

```{r, engine='bash', eval=FALSE}
setenv FSLDIR /backup/crate/neuro_software/fsl
setenv PATH ${FSLDIR}/bin:${PATH}
source ${FSLDIR}/etc/fslconf/fsl.csh
```

##FreeSurfer 

To use [`FreeSurfer`](https://surfer.nmr.mgh.harvard.edu/) add the following to your .cshrc profile:

```{r, engine='bash', eval=FALSE}
setenv FREESURFER_HOME /backup/crate/neuro_software/freesurfer
source $FREESURFER_HOME/SetUpFreeSurfer.csh
```


##R Packages 

These are some useful R packages for neuroimage analysis.  

Install the following packages from CRAN: 

```{r, engine='bash', eval=FALSE}
install.packages("oro.dicom") # working with DICOM images
install.packages("oro.nifti") # working with NIfTI objects 
install.packages("devtools") # Getting GitHub Packages
```

[`fslr`](https://journal.r-project.org/archive/2015-1/muschelli-sweeney-lindquist-etal.pdf) is a port of FSL into R. The most up to date version is found on github:   

```{r, engine='bash', eval=FALSE}
library(devtools) 
install_github("muschellij2/fslr") 
```

[`ANTsR`](http://stnava.github.io/ANTsR/) is a port of the neuroimaging software [`ANTs`](http://picsl.upenn.edu/software/ants/) into R.  This requires cmake to install (which we already have installed on the servers).  You need to first install the [`ITKR`](https://github.com/stnava/ITKR) package before you can install ANTsR.  And installation of ITKR requires instalation of [`cmaker`](https://github.com/stnava/cmaker).  [`extrantsr`](https://github.com/muschellij2/extrantsr) is an R package with extra functions to work with ANTsR: 

```{r, engine='bash', eval=FALSE}
library(devtools) 
install_github("stnava/cmaker") 
install_github("stnava/ITKR") 
install_github("stnava/ANTsR")
install_github("muschellij2/extrantsr")
```


