# sc-metadata-fields
Specifications of the MAGE-TAB format used for [Single Cell Expression Atlas](https://www.ebi.ac.uk/gxa/sc/home)

We have adapted the [MAGE-TAB v1.1 format](http://fged.org/projects/mage-tab/) to capture necessary metadata for single-cell RNA-sequencing experiments to allow automated re-processing. 

### IDF

The IDF (invesigation description format) contains fields describing the study, authors/submitters, protocols, publications. 
We have added further fields as comments used to for configuration of the processing (e.g. expected cluster numbers) and visualisation (e.g. to colour plots by metadata).<br>
[List of IDF fields](IDF_template.txt)

### SDRF

The SDRF (sample data relationship format) describes the samples, cDNA libraries ("extracts"), sequencing assays and their relation to each other. Due to distinct procedures for processing cells and analysing data, we use different formats and fields to describe plated-based experiments (such as Smart-seq2) and droplet-based experiments (such as 10x). For plate-based experiments, we capture single-cell specific metadata such as inferred cell type and single cell well quality. Here, each sample corresponds to a single cell (or well on the plate). For droplet-based experiments, we capture technology-specific metadata that describes the contruction of the library more closely (e.g. where barcodes are located). Here, one sample corresponds to a sequencing library that typically contains a few thousand cells. 

Current templates:
* [SDRF fields for plate-based experiments](SDRF_template_plate.txt)
* [SDRF fields for droplet-based experiments](SDRF_template_droplet.txt)

#### Note

These templates contain all fields used for processing of plate- and droplet-based experiments but they do not represent the list of mandatory fields, nor do they include the list of mandatory sample attibutes curators aim to annotate all samples with.

Please see the [ArrayExpress single-cell submission guide](https://www.ebi.ac.uk/arrayexpress/help/single-cell_submission_guide.html) for more information about the fields and their values.
