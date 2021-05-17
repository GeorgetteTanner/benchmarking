## Info
This repository contains information and variant profiles for samples used to benchmark somatic genome analysis methods in Tanner et al 2021.

Corresponding sequencing datasets are available at https://www.ebi.ac.uk/ena/browser/view/PRJEB28319.

Note that eg. v1r1 corresponds to s1r1 in Tanner et al.

Some files are only available in the accompanying GitHub release due to their size.

Please email medgnt@leeds.ac.uk for any queries or assistance with using the datasets.


## Bulk samples:

{TUMOUR}Acnv.txt - Copy number profile for bulk sample A (100% purity) for each tumour.

{TUMOUR}Bcnv.txt - Copy	number profile for bulk sample B (75% purity) for each tumour.

{TUMOUR}A.vcf - Point mutations profile for bulk sample A (100% purity) for each tumour. 

{TUMOUR}B.vcf -	Point mutations profile for bulk sample B (100% purity) for each tumour.

These contain both germline and somatic mutations. The {TUMOUR}_ccfs.txt file or the germline profile in the individual_clone_profiles_vcf can be used to identify which are somatic or germline variants.

{TUMOUR}_ccfs.txt - The cancer cell fraction of every somatic point variant in each tumour.

## Individual clones (including germline "clone"):

Clone files include information on mutations that occured in that clone as well as all parent clones. Ie. clone3 (which is a direct daughter of clone1) contains all mutations from the germline clone and clone1, as well as those that occured de novo in clone3.

{TUMOUR}{CLONE}cnv.txt - Copy number profile for clone.

{TUMOUR}{CLONE}.vcf - Point mutations profile for clone.

{TUMOUR}{CLONE}variants.txt - Order in which point mutations, CNVs, and aneuploid events occured in the clone.


## Other:

A.txt - Realtive proportions of reads from each clone that were combined to form bulk sample A.

B.txt -	Realtive proportions of reads from each clone that were combined to form bulk sample B.

### HeteroGenesis inputs

{TUMOUR}.json - Input for HeteroGenesis used to simulate tumour.


