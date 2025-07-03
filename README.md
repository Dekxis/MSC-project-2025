# MSC-project-2025
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
