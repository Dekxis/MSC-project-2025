Detecting adapter sequence for read1...
>Nextera_LMP_Read1_External_Adapter | >Illumina Multiplexing Index Sequencing Primer
GATCGGAAGAGCACACGTCTGAACTCCAGTCAC

Detecting adapter sequence for read2...
No adapter detected for read2

Read1 before filtering:
total reads: 770013
total bases: 57750975
Q20 bases: 55098919(95.4078%)
Q30 bases: 52447874(90.8173%)

Read2 before filtering:
total reads: 770013
total bases: 57750975
Q20 bases: 45836358(79.369%)
Q30 bases: 41681413(72.1744%)

Read1 after filtering:
total reads: 173464
total bases: 10855011
Q20 bases: 10600480(97.6552%)
Q30 bases: 10228039(94.2241%)

Read2 after filtering:
total reads: 173464
total bases: 10733374
Q20 bases: 10483770(97.6745%)
Q30 bases: 10161164(94.6689%)

Filtering result:
reads passed filter: 346928
reads failed due to low quality: 315940
reads failed due to too many N: 172
reads failed due to too short: 876986
reads with adapter trimmed: 716081
bases trimmed due to adapters: 19262136

Duplication rate: 44.8925%

Insert size peak (evaluated by paired-end reads): 83

JSON report: fastp.json
HTML report: fastp.html















/storage/aelangov/actual_samples/decontamination_samples/anglosaxon_blank   directory for vikings/anglo saxon
/storage/aelangov/actual_samples/decontamination_samples/roman_blank  directory for roman sample









/storage/aelangov/actual_samples/decontamination_samples/fastqc_reports_before_trim

fam i want to run multiqc again in this directory cuz the previous multiqc was for different samples
also save the output as multiqcblank report inside the decontamination sample folder we created







(decontam_qc_env) [aelangov@login01(Bradford-HPC) ~]$ fastp \
>   -i $IN_DIR/ERR1329876_1.fastq.gz \
>   -I $IN_DIR/ERR1329876_2.fastq.gz \
>   -o $OUT_DIR/ERR1329876_trimmed_1.fastq.gz \
>   -O $OUT_DIR/ERR1329876_trimmed_2.fastq.gz \
>   --detect_adapter_for_pe \
>   --qualified_quality_phred 15 \
>   --length_required 30 \
>   --thread 4 \
>   --html $OUT_DIR/ERR1329876_fastp.html \
>   --json $OUT_DIR/ERR1329876_fastp.json
Detecting adapter sequence for read1...
No adapter detected for read1

Detecting adapter sequence for read2...
No adapter detected for read2

Read1 before filtering:
total reads: 587
total bases: 14675
Q20 bases: 14376(97.9625%)
Q30 bases: 14288(97.3629%)

Read2 before filtering:
total reads: 587
total bases: 14675
Q20 bases: 12686(86.4463%)
Q30 bases: 12452(84.8518%)

Read1 after filtering:
total reads: 0
total bases: 0
Q20 bases: 0(-nan%)
Q30 bases: 0(-nan%)

Read2 after filtering:
total reads: 0
total bases: 0
Q20 bases: 0(-nan%)
Q30 bases: 0(-nan%)

Filtering result:
reads passed filter: 0
reads failed due to low quality: 2
reads failed due to too many N: 0
reads failed due to too short: 1172
reads with adapter trimmed: 0
bases trimmed due to adapters: 0

Duplication rate: 10.0511%

Insert size peak (evaluated by paired-end reads): 0

JSON report: /storage/aelangov/actual_samples/decontamination_samples/fastp_trimmed_blanks/ERR1329876_fastp.json
HTML report: /storage/aelangov/actual_samples/decontamination_samples/fastp_trimmed_blanks/ERR1329876_fastp.html

fastp -i /storage/aelangov/actual_samples/decontamination_samples/roman_blank/ERR1329876_1.fastq.gz -I /storage/aelangov/actual_samples/decontamination_samples/roman_blank/ERR1329876_2.fastq.gz -o /storage/aelangov/actual_samples/decontamination_samples/fastp_trimmed_blanks/ERR1329876_trimmed_1.fastq.gz -O /storage/aelangov/actual_samples/decontamination_samples/fastp_trimmed_blanks/ERR1329876_trimmed_2.fastq.gz --detect_adapter_for_pe --qualified_quality_phred 15 --length_required 30 --thread 4 --html /storage/aelangov/actual_samples/decontamination_samples/fastp_trimmed_blanks/ERR1329876_fastp.html --json /storage/aelangov/actual_samples/decontamination_samples/fastp_trimmed_blanks/ERR1329876_fastp.json
fastp v0.25.0, time used: 1 seconds













(decontam_qc_env) [aelangov@login01(Bradford-HPC) ~]$ OUT_DIR=/storage/aelangov/actual_samples/decontamination_samples/fastp_trimmed_blanks
(decontam_qc_env) [aelangov@login01(Bradford-HPC) ~]$ mkdir -p $OUT_DIR
(decontam_qc_env) [aelangov@login01(Bradford-HPC) ~]$ fastp \
>   -i $IN_DIR/ERR1329876_1.fastq.gz \
>   -I $IN_DIR/ERR1329876_2.fastq.gz \
>   -o $OUT_DIR/ERR1329876_trimmed_1.fastq.gz \
>   -O $OUT_DIR/ERR1329876_trimmed_2.fastq.gz \
>   --detect_adapter_for_pe \
>   --qualified_quality_phred 15 \
>   --length_required 30 \
>   --thread 4 \
>   --html $OUT_DIR/ERR1329876_fastp.html \
>   --json $OUT_DIR/ERR1329876_fastp.json
-bash: fastp: command not found







(decontam_qc_env) [aelangov@login01(Bradford-HPC) ~]$ conda activate decontam_qc_env
(decontam_qc_env) [aelangov@login01(Bradford-HPC) ~]$ multiqc /storage/aelangov/actual_samples/decontamination_samples/fastqc_reports_before_trim \
> -o /storage/aelangov/actual_samples/decontamination_samples/multiqc_before_trim
Illegal instruction (core dumped)



Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use
#
#     $ conda activate decontam_qc_env
#
# To deactivate an active environment, use
#
#     $ conda deactivate

(base) [aelangov@login01(Bradford-HPC) ~]$

 
 
 
 Miniconda3/py311_25.3.1-1    bioconda/Miniconda3-py39_4.10.3


Please check the spelling or version number. Also try "module spider ..."
It is also possible your cache file is out-of-date; it may help to try:
  $ module --ignore_cache load "anaconda"

Also make sure that all modulefiles written in TCL start with the string #%Module



2025-08-04 13:49:49 (1.17 MB/s) - ‘ERR1407493_2.fastq.gz’ saved [8094857]

/tmp/slurmd/job319952/slurm_script: line 42: fastqc: command not found
/tmp/slurmd/job319952/slurm_script: line 46: multiqc: command not found

# MSC-project-2025
/storage/aelangov/actual_samples/decontamination_samples/roman_blank/raw_reads
/storage/aelangov/actual_samples/decontamination_samples/viking_blank/raw_reads

Ancient Oral Microbiome
/storage/aelangov/raw_practice_data/scripts

viking/angalo samples

/storage/aelangov/actual_samples/anglo_viking_samples/norton_on_tees/raw_reads/calculus/fastqc_res

/storage/aelangov/actual_samples/anglo_viking_samples/coppergate_york/raw_reads/calculus/fastqc_res

Roman samaples

/storage/aelangov/actual_samples/roman_samples/driffield_york/raw_reads/calculus/fastqc_res


/storage/aelangov/actual_samples/roman_samples/oxford_leicester/raw_reads/calculus/fastqc_res


(qc_env) [aelangov@login01(Bradford-HPC) scripts]$ module load bioconda
(base) [aelangov@login01(Bradford-HPC) scripts]$ conda activate qc_env
(qc_env) [aelangov@login01(Bradford-HPC) scripts]$ cd /storage/aelangov/actual_samples/roman_samples/oxford_leicester/raw_reads/calculus
(qc_env) [aelangov@login01(Bradford-HPC) calculus]$ mkdir -p fastqc_trimmed_res
(qc_env) [aelangov@login01(Bradford-HPC) calculus]$ fastqc *_trimmed_1.fastq.gz *_trimmed_2.fastq.gz --threads 2 --outdir fastqc_trimmed_res
Skipping '*_trimmed_1.fastq.gz' which didn't exist, or couldn't be read
Skipping '*_trimmed_2.fastq.gz' which didn't exist, or couldn't be read

/storage/aelangov/actual_samples/anglo_viking_samples/coppergate_york/raw_reads/calculus/fastp_trimmed


 ls -lh /storage/aelangov/actual_samples/decontamination_samples/*/*
-rw-r--r-- 1 aelangov domain users    0 Aug  1 17:12 /storage/aelangov/actual_samples/decontamination_samples/centrifuge_blank_reports/roman_blank_centrifugeOutputs.txt
-rw-r--r-- 1 aelangov domain users    0 Aug  1 17:15 /storage/aelangov/actual_samples/decontamination_samples/centrifuge_blank_reports/viking_blank_centrifugeOutputs.txt

/storage/aelangov/actual_samples/decontamination_samples/roman_blank/raw_reads:
total 36K
-rw-r--r-- 1 aelangov domain users 16K Aug  1 17:12 ERR1329876_1.fastq.gz
-rw-r--r-- 1 aelangov domain users 18K Aug  1 17:12 ERR1329876_2.fastq.gz

/storage/aelangov/actual_samples/decontamination_samples/viking_blank/raw_reads:
total 28K
-rw-r--r-- 1 aelangov domain users 12K Aug  1 17:12 ERR1329877_1.fastq.gz
-rw-r--r-- 1 aelangov domain users 13K Aug  1 17:12 ERR1329877_2.fastq.gz





[aelangov@login01(Bradford-HPC) scripts]$ zcat /storage/aelangov/actual_samples/decontamination_samples/roman_blank/raw_reads/ERR1329876_1.fastq.gz | head
@ERR1329876.1 MS9_18466:1:1101:13876:2259#53/1
AGTTGAACAAAAAGACTTGCCAGGT
+
>AABBFFFFFFFGGCGGGGGGGGHG
@ERR1329876.2 MS9_18466:1:1101:14918:3196#53/1
TTACTTCTAGATCGGAAGAGCACAC
+
3AAABFFFFFBFGEFGCGGGGGHHH
@ERR1329876.3 MS9_18466:1:1101:13893:3650#53/1
TTACTTCGCTCGGTGATCGCGATCT
