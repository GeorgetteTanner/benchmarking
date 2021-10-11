## Info
This repository contains information and variant profiles for samples used to benchmark somatic genome analysis methods in Tanner et al.

Some files are only available in the accompanying GitHub release due to their size.

Note that eg. v1r1 corresponds to s1r1 in Tanner et al.

Corresponding sequencing datasets are available at https://www.ebi.ac.uk/ena/browser/view/PRJEB28319.

Please email medgnt@leeds.ac.uk for any queries or assistance with using the datasets.


## Bulk samples:

{TUMOUR}Acnv.txt - Copy number profile for bulk sample A (100% purity) for each tumour.

{TUMOUR}Bcnv.txt - Copy	number profile for bulk sample B (75% purity) for each tumour.

{TUMOUR}Ecnv.txt - Copy	number profile for bulk sample E (50% purity) for each tumour.

{TUMOUR}Fcnv.txt - Copy	number profile for bulk sample F (25% purity) for each tumour.

v2r1Ccnv.txt - Copy number profile for bulk sample with linear topology and 3 clones for tumour s2r1.

v2r1Dcnv.txt - Copy number profile for bulk sample with branched topology and 5 clones for tumour s2r1.

Bulk CNV files provide the absolute copy number profiles for each sample, which includes the effects of germline CNVs. To generate somatic CNV profiles (which will be identical for all purities for the same sample), the ratio of 100% pure tumour bulk sample copy numbers to germline copy numbers is calculated for each allele:
{TUMOUR}Acnv_d_{TUMOUR}germlinecnv.bed 

VCF files available in the Release1 data:

{TUMOUR}A.vcf - Point mutations profile for bulk sample A (100% purity) for each tumour. 

{TUMOUR}B.vcf -	Point mutations profile for bulk sample B (75% purity) for each tumour.

{TUMOUR}E.vcf -	Point mutations profile for bulk sample E (50% purity) for each tumour.

{TUMOUR}F.vcf -	Point mutations profile for bulk sample F (25% purity) for each tumour.

These contain both germline and somatic mutations. The {TUMOUR}_ccfs.txt file or the germline profile in the individual_clone_profiles_vcf can be used to identify which are somatic or germline variants.

{TUMOUR}_ccfs.txt - The cancer cell fraction of every somatic point variant in each tumour.

v2r1_ccfs_branched.txt - The cancer cell fraction of every somatic point variant in the branched topology 5 clone sample for tumour s2r1.

v2r1_ccfs_linear.txt - The cancer cell fraction of every somatic point variant in the linear topology 3 clone sample for tumour s2r1.

## Individual clones (including germline "clone"):

Clone files include information on mutations that occured in that clone as well as all parent clones. Ie. clone3 (which is a direct daughter of clone1) contains all mutations from the germline clone and clone1, as well as those that occured de novo in clone3.

{TUMOUR}{CLONE}cnv.txt - Copy number profile for clone.

{TUMOUR}{CLONE}.vcf - Point mutations profile for clone.

{TUMOUR}{CLONE}variants.txt - Order in which point mutations, CNVs, and aneuploid events occured in the clone.


## Other:

{SAMPLE}.txt - Realtive proportions of reads from each clone that were combined to form bulk sample {SAMPLE}.

### HeteroGenesis inputs

{TUMOUR}.json - Input for HeteroGenesis used to simulate tumour.


## code:

cnvkit_modifications - To use these files they should be substituted in for equivaent files in the the CNVkit library.
