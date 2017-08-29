Overview
========

As part of Illumina's Platinum Genomes project we have derived a set of
high-confidence and phased variant calls for NA12877 and NA12878. We did this 
by taking into account the inheritance constraints in the pedigree and the
concordance of variant calls across different methods.

Please cite our submitted manuscript in publications and other public usage of
Platinum Genomes: http://biorxiv.org/content/early/2016/05/26/055541

If you have any questions, contact us at: platinumgenomes@illumina.com.
Please note that, while Platinum Genomes are freely available, Illumina does not
offer technical support for these resources.


Version history
===============

Version: 2016-1.0
Data: SNVs and small indels for hg38 and hg19
Date: 6 June 2016
---------------------------------------------
- Submission of manuscript.
- Implementation of k-mer filtering.
- ConfidentRegions.bed is now the same for all pedigree members.
- Clean-ups in the VCFs: less cluttered INFO fields and removal
  of non-PASSing records.
- Change of versioning scheme: hg38 and hg19 builds are now released together
  in the same bundle under a common release id.

Version: hg19/8.0.1, hg38/2.0.1
Data: SNVs and small indels for hg38 and hg19
Date: 3 August 2015
----------------------------------------------
- Include truth data that is natively built on hg38.
- Simplifications in the back-end processing workflow.
- Changes in the formatting of the VCFs.
- Introduction of "silver" variant calls.

Version: IlluminaPlatinumGenomes_v7.0
Data: SNVs and small indels for hg19
Date: 22 December 2014
--------------------------------------
- Refresh isaac and bwa_gatk call sets with newer versions of the pipelines
- Use vcfallelicprimitives for decomposition of complex variant calls
- Small fixes in the formatting of the VCFs

Version: IlluminaPlatinumGenomes_v6.0
Data: SNVs and small indels for hg19
Date: 21 November 2014
--------------------------------------
- First public release of PG truth data


Variant calling methods used for Platinum Genomes
=================================================

For the hg38 build
------------------
- bwa_freebayes: bwa-mem-0.7.12, freebayes-0.9.21 (joint calling mode), SNVs and indels
- bwa_gatk: bwa-mem-0.7.12, gatk-3.2.2 (joint calling mode), SNVs and indels
- bwa_platypus: bwa-mem-0.7.12, platypus-0.8.1 (joint calling mode), SNVs and indels
- isaac_strelka: isaac_aligner-02.15.02.28, isaac_variant_caller-2.1.4.2 (now known as strelka), SNVs and indels

For the hg19 build
------------------
- bwa_freebayes: bwa-mem-0.7.5, freebayes-0.9.1 (joint calling mode), SNVs and indels
- bwa_gatk: bwa-mem-0.7.5, gatk-3.2.2 (joint calling mode), SNVs and indels
- bwa_platypus: bwa-mem-0.7.5, platypus-0.7.2 (joint calling mode), SNVs and indels
- cgi: CGTools-2.0, SNVs only
- cortex: cortex-1.0.5.11, SNVs and indels
- isaac_strelka: isaac_aligner-02.14.10.23, isaac_variant_caller-2.1.4.1 (now known as strelka), SNVs and indels