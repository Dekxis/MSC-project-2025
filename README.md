> /storage/aelangov/actual_samples/decontamination_samples/roman_blank/ERR1329876_1.fastq.gz
application/gzip
Started analysis of ERR1329876_1.fastq.gz
Analysis complete for ERR1329876_1.fastq.gz
(decontam_qc_env) [aelangov@login01(Bradford-HPC) ~]$
 
 
 
 
 
 
 
 ls -lh /storage/aelangov/actual_samples/decontamination_samples/roman_blank/raw_reads/
ls: cannot access '/storage/aelangov/actual_samples/decontamination_samples/roman_blank/raw_reads/': No such file or directory

/storage/aelangov/actual_samples/decontamination_samples/roman_blank

fastqc -o ~/decontam_fastqc_test \
> /storage/aelangov/actual_samples/decontamination_samples/roman_blank/raw_reads/ERR1329876_1.fastq.gz
Skipping '/storage/aelangov/actual_samples/decontamination_samples/roman_blank/raw_reads/ERR1329876_1.fastq.gz' which didn't exist, or couldn't be read
(decontam_qc_env) [aelangov@login01(Bradford-HPC) ~]$







(decontam_qc_env) [aelangov@login01(Bradford-HPC) ~]$ module load Miniconda3/py311_25.3.1-1
(base) [aelangov@login01(Bradford-HPC) ~]$ eval "$($(which conda) shell.bash hook)"
usage: conda [-h] [-v] [--no-plugins] [-V] COMMAND ...
conda: error: argument COMMAND: invalid choice: '()' (choose from 'activate', 'clean', 'commands', 'compare', 'config', 'content-trust', 'create', 'deactivate', 'doctor', 'env', 'export', 'info', 'init', 'install', 'list', 'notices', 'package', 'remove', 'rename', 'repoquery', 'run', 'search', 'tos', 'uninstall', 'update', 'upgrade')
(base) [aelangov@login01(Bradford-HPC) ~]$ conda activate decontam_qc_env
(decontam_qc_env) [aelangov@login01(Bradford-HPC) ~]$ fastqc -o ~/decontam_fastqc_test \
> /storage/aelangov/actual_samples/decontamination_samples/roman_blank/raw_reads/ERR1329876_1.fastq.gz
Specified output directory '/home/aelangov/decontam_fastqc_test' does not exist
(decontam_qc_env) [aelangov@login01(Bradford-HPC) ~]$









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
