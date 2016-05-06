# Fastq Quality Trimming Tool

A tool that trims reads based on quality score from a FastQ file.  Requires FastQ input file and quality score conversion table. Optionally accepts user-specified quality score trim threshold, sliding window size, minimum read length, output file type, and output file name. If no input is specified for optional parameters, the following defaults are used:  
 
* Threshold score: 20  
* Window size: 4  
* Minimum read length: none  
* Output file type: FastQ  
* Output file name: "output"  

For more complete documentation, see [the Yale CBB752 course website](http://cbb752spring2016.github.io/QCStep#sequence-read-trimming).

Note: This tool is part of a set of bioinformatic and biological structure tools created for CBB752 at Yale University in the Spring 2016. The website containing links to the set of tools can be found at: <https://github.com/CBB752Spring2016/CBB752Spring2016.github.io>.

***
  
## Usage

Download "QualityTrim.R" and "qscores.txt", and optionally the example input file provided.
  
  Usage: 
  
```Rscript QualityTrim.R -i <input fastq file> -s <qscore file> -t <threshold cutoff score> -f <output file format {fastq, fasta, both}> -m <minimum read length> -o <output file base name>```
  
  
  Example: 
  
```Rscript QualityTrim.R -i example.fastq -s qscore.txt -t 25 -f fastq -m 10 -o outputfile```
  
  An example output is shown as output_R.fasta and output_R.fastq

***  

This tool has also been implemented [in python by wellshl](https://github.com/wellshl/CBB752_Final_Project_1.3).