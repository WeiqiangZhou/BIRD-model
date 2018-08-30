# BIRD prediction models
This repository contains the prebuilt models for BIRD.
There are three models available:
1. RNA-seq model: 
https://github.com/WeiqiangZhou/BIRD-model/releases/download/v1.2/RNAseq_model_file.bin.zip

2. RNA-seq model for 2 million loci: 
https://github.com/WeiqiangZhou/BIRD-model/releases/download/v1.0/RNAseq_model_file_2M.bin.zip

3. Exon Array model:
https://github.com/WeiqiangZhou/BIRD-model/releases/download/v1.1/Exonarray_model_file.bin.zip

## How to use
1. Download and unzip the required model from this repo.
```
wget https://github.com/WeiqiangZhou/BIRD-model/releases/download/v1.2/RNAseq_model_file.bin.zip
unzip RNAseq_model_file.bin.zip
```
You will get the model file: RNAseq_model_file.bin.

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
path_to_BIRD/BIRD_predict -b path_to_model/RNAseq_model_file.bin -i FPKM_data_matrix.txt -o output_file.txt
```

**More instructions for BIRD can be found in https://github.com/WeiqiangZhou/BIRD**

