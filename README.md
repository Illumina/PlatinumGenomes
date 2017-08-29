# Platinum Genomes

This repo contains the Platinum Genomes small variant truthset for samples NA12878 (also known as hg001) and NA12877.
Platinum Genomes truthset variants were validated using haplotype inheritance information through a well studied 
17-member pedigree (CEPH 1463).

## Truthsets

Truthsets are made up of a VCF of validated variant records and a BED file of confident regions. These files
can be downloaded from the AWS S3 bucket `platinum-genomes`, for example using the
[AWS CLI](https://aws.amazon.com/cli/):

```bash
aws s3 cp s3://platinum-genomes/2017-1.0 pg2017 --recursive
```

If you don't have AWS credentials, you can use `wget` or similar with the [file URIs in this repo](files/), e.g.:

```bash
wget -xi files/2016-1.0.files
```

You can then use the relevant md5 checksum in each release to validate data integrity.

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
