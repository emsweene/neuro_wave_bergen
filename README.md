# neuro_wave_bergen
Setup for using common neuroimaging software on the wave and bergen servers at Rice. 

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

Install the following packages from github: 

```{r, engine='bash', eval=FALSE}
library(devtools) 
install_github("muschellij2/fslr") 
install_github("muschellij2/extrantsr")
```
