# STAR
Code for [Spatio-Temporal Graph Transformer Networks for Pedestrian Trajectory Prediction](https://arxiv.org/abs/2005.08514)

### Environment

The code is tested on GTX 1080Ti, Python 3.6.3, numpy 1.17.5, pytorch 1.1.0 and CUDA9.0.

### Train

The Default settings are to train on ETH-univ dataset. 

Data cache and models will be stored in the subdirectory "./output/eth/" by default. Notice that for this repo, we only provide implementation on GPU.

```
git clone https://github.com/Majiker/STAR.git
cd STAR
python trainval.py
```

Configuration files are also created after the first run, arguments could be modified through configuration files or command line. 
Priority: command line \> configuration files \> default values in script.

The datasets are selected on arguments '--test_set'. Five datasets in ETH/UCY including
[**eth, hotel, zara1, zara2, univ**].

### Example

This command is to train model for ETH-hotel and start test at epoch 10. For different dataset, change 'hotel' to other datasets named in the last section.

```
python trainval.py --test_set hotel --start_test 10'
```

During training, the model for Best FDE on the corresponding test dataset would be record.


### Reference

The code base heavily borrows from [SR-LSTM](https://github.com/zhangpur/SR-LSTM)
