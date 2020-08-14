This repository contains the prebuilt models for BIRD.

## BIRD prediction models for human reference genome hg19

There are four models available for hg19:
1. RNA-seq model based on FPKM, current release (trained with 167 ENCODE samples):
https://github.com/WeiqiangZhou/BIRD-model/releases/download/v1.3/human_hg19_model.bin.zip

2. RNA-seq model based on FPKM, previous release (trained with 70 Epigenome Roadmap samples): 
https://github.com/WeiqiangZhou/BIRD-model/releases/download/v1.2/RNAseq_model_file.bin.zip

3. RNA-seq model based on FPKM for 2 million loci, previous release (trained with 70 Epigenome Roadmap samples): 
https://github.com/WeiqiangZhou/BIRD-model/releases/download/v1.0/RNAseq_model_file_2M.bin.zip

4. Exon Array model:
https://github.com/WeiqiangZhou/BIRD-model/releases/download/v1.1/Exonarray_model_file.bin.zip

## BIRD prediction models for human reference genome hg38

1. RNA-seq model based on FPKM, current release (trained with 167 ENCODE samples):
https://github.com/WeiqiangZhou/BIRD-model/releases/download/v1.4/human_hg38_model.bin.zip

## How to use
1. Download and unzip the required model from this repo. For prediction based on RNA-seq data, we suggest users use the current release.
```
wget https://github.com/WeiqiangZhou/BIRD-model/releases/download/v1.3/human_hg19_model.bin.zip
unzip human_hg19_model.bin.zip
```
You will get the model file: human_hg19_model.bin.

2. Install BIRD using the source code.
```
wget https://github.com/WeiqiangZhou/BIRD/archive/master.zip
unzip master.zip
cd BIRD-master
make
```

3. Prediction using the model file.

Suppose you store the model files in _path_to_model_ and install BIRD in _path_to_BIRD_.

Run:
```
path_to_BIRD/BIRD_predict -b path_to_model/human_hg19_model.bin -i FPKM_data_matrix.txt -o output_file.txt
```

**More instructions for BIRD can be found in https://github.com/WeiqiangZhou/BIRD**

