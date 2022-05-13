## Summary
1. From publication to IDR study, viewing images and ROIs
2. From Gene to phenotypes, orientating in metadata ecosystem
3. From metadata to analytics, using metadata to QA the results


## Walkthrough 

### From publication to IDR study, viewing images and ROIs
Start from PubMed search engine. Search for three terms, “Blin”, “Lowell” and “segmentation”. First result will be a paper from Blin et al from Sally Lowell’s lab published in PLOS Biology in 2019.
Click on the icon in top-right for full text of the paper in PLOS Biology
Inside the paper, navigate to the Data availability section and then go from there to the starting page at [IDR homepage](http://idr.openmicroscopy.org/) and search for a “Name (IDR number)”. (the default option). Enter the “62” into the second search box. Accept the suggestion and click on the thumbnail. This gives you all the images contained in the idr0062 study..This workflow shows one of the main uses of IDR for data visibility, Quality Control for publishers and community. 
In the idr0062 study, on the image http://idr.openmicroscopy.org/webclient/?show=image-6001239 we can see the attached tiff file with ROIs. These ROIs were extracted into OMERO ROIs (masks), which can be seen overlaid onto the images.
To see the ROIs, double-click onto the thumbnail of the image in the central pane. This will open the full viewer, called OMERO.iviewer.
Select the ROIs tab inside OMERO.iviewer. The mask ROIs will load.
Return to OMERO.web in the next tab of your browser.
Click on the Experiment (named idr0062-blin-nuclearsegmentation/experimentA)  and expand the “Attributes”' harmonica in the right-hand pane. Find and click on the DOI of the paper link. We will now continue this workflow using [Jupyter notebook](0_Python_API.ipynb) and OMERO API. The other GUI workflows below are for your information only.

### From Gene to Phenotypes  (FYI only, not shown)
Start from idr.openmicroscopy.org. Select Attribute Gene. Search for KRAS. In the results, find the study idr0033A. This is a gene overexpression study by Rohban et al. Click on the “More.. link in the same line to the right of it. You are navigated into the IDR. Select the image http://idr.openmicroscopy.org/webclient/?show=image-3194247 . 
Study the right-hand pane and find the “Gene” block in Attributes harmonica. Click on the icon in the Gene Identifier line. This will lead you to NCBI. Go back to the IDR and scroll down in the Attributes. Find the “low cell density” in one of the Phenotype metadata blocks. Click on the CMPO_000052 link underneath it. This navigates to the search results page with all the images associated with this ontology term. Select the top level node in the left-hand side and study the right-hand pane to see the standardization work done on the CMPO_000052 “decreased cell numbers” phenotype. 
Start typing in the box above the left-hand side pane to search for images associated with other phenotypes inside IDR. 
Go back to the KRAS search results by clicking the back arrow in your browser. Select one image in central pane, click onto the chain icon in the top of the right-hand pane and copy the link. Paste the link into a new tab of your browser. This navigates you to the full Plate view. The image you were seeing inside the KRAS results is now highlighted in the context of the whole Plate.
### From compound to analytics (FYI only, not shown)
Start from idr.openmicroscopy.org. Select Attribute Compound. Search for Remdesivir. In the results, the study idr0094B is shown. Click on More… This leads to inside the IDR. Select the first image in the first container.
In the right-hand pane, scroll down to Others section of the Attributes harmonica. Note the DPC number and compare with the density of the cells in the thumbnail. The DPC is showing the effectiveness of the Remdesivir compound against the cytotoxic effects of the Sars-Cov-2 virus. The higher the DPC, the more intact the human cell monolayer in the images. Compare this with the Remdesivir concentration, which is to be found in the same Attributes harmonice, above in the Compound supplementary section.
