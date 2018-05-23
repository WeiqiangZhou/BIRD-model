# BIRD-model
This repository contains the prebuilt models for BIRD.

# How to use
1. Download and unzip the required model from this repo.
```
wget https://github.com/WeiqiangZhou/BIRD-model/releases/download/v1.0/model_file_2M.zip
unzip model_file_2M.bin.zip
```
You will get two files: model_file_2M.bin and gene_name.txt.

2. Install BIRD using the source code.
```
wget https://github.com/WeiqiangZhou/BIRD/archive/master.zip
unzip master.zip
cd BIRD-master
make
```

3. Prediction using the model file.

If you store the model files in _path_to_model_ and install BIRD in _path_to_BIRD_.

Prepare input:
```
Rscript --vanilla path_to_BIRD/R_script/match_input_matrix.r path_to_model/gene_name.txt FPKM_data_matrix.txt FPKM_data_matrix_match.txt
```
Prediction:
```
path_to_BIRD/BIRD_predict -b path_to_model/model_file_2M.bin -i FPKM_data_matrix_match.txt -o output_file.txt
```

**More instruction for BIRD can be found in https://github.com/WeiqiangZhou/BIRD**

