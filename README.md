# **DeepTriplet**

## Introduction
DeepTriplet is a Deep Learning-based Model for pMHC-TCR Binding Prediction.
![preview](https://github.com/wanghwlab/DeepTriplet/blob/main/Img/Pic_Framework.png)

## How to install DeepTriplet
To install DeepTriplet, make sure you have installed [PyTorch](https://pytorch.org/). If you need more details on the dependences, look at the requirements.txt file.

- Clone the repository.
```shell
git clone https://github.com/wanghwlab/DeepTriplet.git
```

- Create a virtual environment by conda.
```shell
conda create -n DeepTriplet python=3.9 -y
conda activate DeepTriplet
```

- Install DeepTriplet from shell.
```shell
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu121
pip install -r requirements.txt
```

*Note* : The installation of pytorch needs to correspond to your system, GPU and other versions, please check [PyTorch Version](https://pytorch.org/get-started/locally/).

## How to Use DeepTriplet
Using DeepTriplet for predicting triplet outcomes requires modifying the input file path and setting the prediction threshold in DeepTriplet.py. The default threshold is set to 0.58.


## How to run DeepTriplet for binding prediction
For prediction, please prepare your Triplet data and place them in a .csv file format similar to the test/test.csv provided. 

```python
python DeepTriplet.py
```

- **Input**: input csv file with 3 columns named as "CDR3, Peptide, HLA_type": TCR CDR3β sequence, peptide sequence, and HLA allele.
![preview](https://github.com/wanghwlab/DeepTriplet/blob/main/Img/example_input_file.png)
- **Output**: diretory you want to save the output
- **Output_log**: The local directory is used for log files, containing input triplet data, prediction progress, result statistics, and more.

## Expected output
DeepTriplet outputs a table with 5 columns: CDR3 sequences, Peptide sequences, HLA alleles, Prediction Binding Score, and Label for each pair of Triplet. 

![preview](https://github.com/wanghwlab/DeepTriplet/blob/main/Img/example_output_file.png)

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
