# Degradomics - the study of proteolytic processing

Degradomics is the study of proteolysis, i.e., the study of proteolytic cleavage of proteins. A commonly applied experimental methodology to study and detect proteolysis is LC-MS/MS proteomics.
```{margin} LC-MS/MS
LC-MS/MS = liquid chromatography mass spectrometry
```

## A challenge for degradomics data processing 
Proteomics data can be assigned to peptides / proteins by comparison of experimentally observed precursor and fragment mass/charges, with predicted values. 

```{math}
:label: equation_label
\frac{m}{z} = \frac{mass}{charge}
```

Should the experimentally observed precursor and fragment ion m/z values of a spectrum match to a predicted m/z within a defined range, then the spectrum is assigned to that peptide sequence.

 ```{figure} ../fragment_spectrum-01.png
 ---
 height: 300px
 name: example fragment spectrum
 ---
 example of an MS/MS fragment spectrum
 ```

A problem arises, in that the greater the number of possible values that a peptide can be assigned, then the higher the chance of a false positive assignment. Thus, increasing the 'search space', reduces the statistical power of a study.

```{warning}
The choice of database used to search proteomics data can have a great effect on the validity of the conclusions drawn from analysis
```

In degradomics, we are forced to increase the search space in order to allow detection of cleaved peptides. These peptides are termed 'semi-tryptic', in that they possess one or more termini that are not derived from cleavage with trypsin (see below): 

 ```{figure} ../semi-tryptic-01.png
 ---
 height: 300px
 name: semi-tryptic_peptides
 ---
 differences between tryptic and semi-tryptic peptides
 ```
Assigned peptide and proteins are then quantified. Quantification can be performed in a variety of ways, however, comparison between samples of relative intensities of TMT-isobaric tags intensities is a commonly applied method.

 ## Protein vs peptide - level analysis
 A complication in biological interpretation of degradomics datasets, is that a peptide that is significantly different in abundance, may be so simply as a consequence of increased protein-level detection. In degradomics, we are typically more interested in semi-tryptic peptides that significantly differ in quantity, pertaining to proteins that are not significantly different in abundance  
 
 ```{math}
:label: another_label
peptide \not\propto protein
```

```{note}
A semi-tryptic peptide that is increased in quantity where the protein level is also increased doesn't necessarily rule out biological significance
```