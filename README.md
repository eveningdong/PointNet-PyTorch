## PointNet
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

### Predict
Put `*_data.npy` files in a folder.
```
python3 pred_segmentation.py --model path_to_checkpoint --input path_to_input_dir --output path_to_output_dir
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
