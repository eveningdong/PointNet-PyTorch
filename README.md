## PointNet
Reimplementation of PointNet for point cloud segmentation.

This is an (re-)implementation of [PointNet: Deep Learning on Point Sets for 3D Classification and Segmentation](https://arxiv.org/abs/1612.00593) in PyTorch for point cloud segmentation. The implementation is based on PointNet's original implementation in [TensorFlow](https://github.com/charlesq34/pointnet). The code is optimized for limited memory and GPU memory.

### Environment
```
Ubuntu 18.04 LTS
CUDA 10.1
cuDNN 7.0
python 3.6
```

### Install
```
pip3 install torch torchvision
pip3 install -r requirements.txt
```

### Data
Put `train` dataset under `data/train`, `val` dataset under `data/val` and `test` dataset under `data/test`.  
Run `python3 preprocess.py`.

### Train
```
python3 train_segmentation.py
```

### Test
```
python3 test_segmentation.py --model path_to_checkpoint
```

### Visualize
Visualize the data (.npy).
```
python3 visualize.py --path path_to_data
```
Visualize the segmentation (.npy).
```
python3 visualize.py --path path_to_data --label path_to_label
```
