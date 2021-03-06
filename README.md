# GBS_barcode

This script split GBS fastq file by barcode sequences. 

## Getting Started
Usage: GBS_barcode.pl yourBarCodeFile yourEnzymeFile  

You will need to create two text files first, a barcode file and an enzyme file.
Barcode File Example (see the example file, tab delimited text file with 4 columns, code p for paired end, you will need to provide the first end file under the file column :
  
**SampleName**|**code**|**paired**|**file**
-----|-----|-----|-----
s1|CTCC|s|my\_1.fastq  
s2|TGCA|s|my\_1.fastq  
s3|ACTA|s|my\_1.fastq  
s4|GTCT|s|my\_1.fastq  
s5|GAAT|s|my\_1.fastq  
s6|GCGT|s|my\_1.fastq  
s7|TGGC|s|my\_1.fastq  
s8|CGAT|s|my\_1.fastq  
s9|CTTGA|s|my\_1.fastq  
s10|TCACC|s|my\_1.fastq  
s11|CTAGC|s|my\_1.fastq  
s12|ACAAA|s|my\_1.fastq  
s13|TTCTC|s|my\_1.fastq  
s14|AGCCC|s|my\_1.fastq  


Enzyme File Example (ApeKI):

Enzyme: C[AT]GC  
FinalSize: 64  
Ends: GCTGGATC,GCAGGATC,GCTGAGAT,GCAGAGAT,GCAGC,GCTGC  
EnzymeEndSize: 4  
  

Note:
* If you works in Linux or Mac environment, you can use gzip compressed Illumina files directly, as long as the file names end with .gz.
* In barcode file, "s" refere to single end Illumina data, "p" refer to paired end Illumina data. For paired end data files, you only need to provide the first file (with _1 in file name). The second file should have "_2" in file name, and will automatically be recognized.
* In the enzyme file, you are required to provide final size. If reads are shorter than the final size after trimming of the barcode and 3' adapter, the read will be padded with "N" at 3' end. 
* Some sample enzyme files are provided here.

### Prerequisites


### Installing

Download the PERL script.

## Authors

* **Qi Sun**

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments
