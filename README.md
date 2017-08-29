# Platinum Genomes

This repo contains the Platinum Genomes small variant truthset for samples NA12878 (also known as hg001) and NA12877.
Platinum Genomes truthset variants were validated using haplotype inheritance information through a well studied 
17-member pedigree (CEPH 1463).

## Truthsets

Truthsets are made up of a VCF of validated variant records and a BED file of confident regions. Download
these files either by cloning this repository (for the latest release), or by downloading an archive of
a specific [tagged release](https://git.illumina.com/bmoore1/platinum-genomes/releases).

Note this repo uses [git LFS](https://git-lfs.github.com/) to track large files more efficiently. If you want a
full checkout you need to install git LFS (e.g. for OS X: `brew install git-lfs`). Then use `git clone` as normal.

You can also download selected files through the github web UI, for example:
* [NA12878 hg38 truth VCF file](truthsets/hg38/NA12878.vcf.gz)
* [NA12878 hg38 confident regions BED file](truthsets/hg38/ConfidentRegions.bed.gz)

Finally, truthset files can also be downloaded via [FTP](ftp://platgene_ro:''@ussd-ftp.illumina.com/), e.g.:

```sh
wget ftp://platgene_ro:''@ussd-ftp.illumina.com/2016-1.0/hg38/small_variants/NA12878/NA12878.vcf.gz
```

### Usage

To compare a VCF against these truthsets, we recommend using [hap.py](https://github.com/Illumina/hap.py) which
performs a sophisticated haplotype comparison rather than a simpler tool such as `bcftools isec`.

Applications wrapping hap.py and containing these truthsets are available on the following platforms:
* BaseSpace Sequence Hub (VCAT and hap.py applications)
* PrecisionFDA (GA4GH Benchmarking)

## Details

See the attached [wiki](../../wiki) for technical information.

## Raw data

Sequencing data for NA12878, NA12877 and samples NA12889-NA12892 (grandparents) are available through
the ENA:
* [ENA Study: PRJEB3381](https://www.ebi.ac.uk/ena/data/view/PRJEB3381)

BaseSpace users can access this data via a shared BaseSpace project:
* [BaseSpace project share](https://basespace.illumina.com/s/2K7LqNG7Mt1h)

Sequencing data for the remaining pedigree members is not consented for public release and so is 
made available through the dbGaP database:
* [dbGaP: phs001224.v1.p1](https://www.ncbi.nlm.nih.gov/projects/gap/cgi-bin/study.cgi?study_id=phs001224.v1.p1)

## Issues

Please open an [issue](/../../issues/) for comments, issues and other feedback.

## Citation

For further information or to cite Platinum Genomes resources, see:
* Eberle, MA _et al._ (2017) A reference data set of 5.4 million phased human variants validated by genetic inheritance from sequencing a three-generation 17-member pedigree. _Genome Research_, 27:157-164. doi:[10.1101/gr.210500.116](http://dx.doi.org/10.1101/gr.210500.116)