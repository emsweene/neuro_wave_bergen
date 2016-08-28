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
