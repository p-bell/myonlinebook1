# Welcome to Degradomics analysis in Jupyter Lab

This is a short book, to get you started with analysis of proteomics datasets - specifically, with a focus on degradomics. 


## Intended learning outcomes
By the end of this book you will be able to use JupyterLabs / R to identify proteolytic processing in data processed using MSFragger within Fragpipe {cite}`kong2017fragger`

```{tip}
Other MS analysis pipelines are available, however Fragpipe is the quickest I have tested for semi-specific searching of mass spectrometry data
```

 ```{figure} ../example_input_image.png
 ---
 height: 300px
 name: example data
 ---
 How can we find evidence of proteolytic processing here?
 ```

In {numref}`example data`, we can see an example of the output from MSFragger - but how can we better visualise this data in order to discovery evidence of proteolytic processing?  

This book shows an example of analyses and plots that can be readily implemented, in order to obtain evidence of proteolytic processing within your data.

```{margin} Did you know?
Proteolytic processing can generate new protein functions, as well as abolishing protein function
```

 ```{figure} ../example_output_image.png
 ---
 height: 300px
 name: example output
 ---
 From here, we begin biological interpretation of the data
 ```
{numref}`example output`, shows an example of how we can visualise the data in the form of a volcano plot, to better interpret the dataset.

## Caveats
This short book does not go in-depth into generation of the source files used for analysis – check out the Fragpipe manual {cite}`fragpipe_man` for more information. To download FragPipe software, visit {cite}`fragpipe_github`.

```{warning}
Fragpipe requires msconvert from ProteoWizard to process vendor raw data. ProteoWizard does not currently offer Mac (macOS) native support
```

## Dataset used
Our analysis will be applied to a publically available dataset, comparing the proteomes of SARS-CoV-2 infected cells vs controls {cite}`duncan2021` 

Raw peptide and protein abundances have been log2 transformed by Fragpipe as follows:

```{math}
:label: log2abundance
abundance_{transformed} = log_{2}abundance_{raw}
```

The transformation of data applied in {eq}`log2abundance` is important to remember, since it affects post-processing.   

Should non-transformed abundances be required for any other purpose, the following transformation can be applied:
```{math}
:label: 2power
abundance_{raw} = 2^(log_{2}abundance_{transformed})
```
Equally, the use of non-transformed abundances derived by {eq}`2power` can be problematic, due to the inherent non-normality of the data. 


## Additional reading material about degradomics 
To find out more about proteolytic processing and degradomics, check out {cite}`overall2002`


## Bibliography
```{bibliography}
```


