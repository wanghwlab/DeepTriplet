# **DeepTriplet**

## Introduction
DeepTriplet is a Deep Learning-based Model for Predicting **HLA Class-I** TCR-pMHC **Triplet** Antigen Binding Prediction.
![preview](https://github.com/wanghwlab/DeepTriplet/blob/main/img/Pic_Framework.png)

## How to install DeepTriplet
To install DeepTriplet, make sure you have installed [PyTorch](https://pytorch.org/). If you need more details on the dependences, look at the requirements.txt file.

- Set up conda environment for DeepTriplet
```shell
conda create -n DeepTriplet python=3.9 -y
conda activate DeepTriplet
```

- Install DeepTriplet from shell
```shell
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
pip install -r requirements.txt
```

*Note* : The installation of pytorch needs to correspond to your system, GPU and other versions, please check [PyTorch Version](https://pytorch.org/get-started/locally/).

## How to Use DeepTriplet
Using DeepTriplet to achieve different tasks, please import corresponding module to your jupyter notebooks or scripts. 


## How to run DeepTriplet for binding prediction
For sequence-level prediction, please prepare your antigen-HLAI data and place them in a .csv file format similar to the test_antigenHLAI/sequence/test.csv provided. The column 'label' is optional. 

```python
python DeepTriplet.py
```

- **Input**: input csv file with 3 columns named as "CDR3, Peptide, HLA_type": TCR CDR3β sequence, peptide sequence, and HLA allele.
![preview](https://github.com/wanghwlab/DeepTriplet/blob/main/img/example_input_file.png)
- **Output**: 
- **Output_log**: 

## Expected output
DeepTriplet outputs a table with 4 columns: CDR3 sequences, Peptide sequences, HLA alleles, and Prediction Binding Score for each pair of Triplet. 
![preview](https://github.com/wanghwlab/DeepTriplet/blob/main/img/example_output_file.png)

## Citation
```tex
@article{,
  title={},
  author={},
  journal={},
  doi={},
  year={},
  publisher={}
}
```

## Contact
If you have any questions, please contact us at [yanglei59@mail2.sysu.edu.cn](mailto:yanglei59@mail2.sysu.edu.cn) or [wanghw0425@gmail.com](mailto:wanghw0425@gmail.com).
