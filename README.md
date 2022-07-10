# about 

- test repo for [Lift, Splat, Shoot](https://github.com/nv-tlabs/lift-splat-shoot)

# run test 

- segmentation 
    - fix dataset path based on [this](https://github.com/nv-tlabs/lift-splat-shoot/issues/23)
    - fix minor issues based on [this](https://github.com/nv-tlabs/lift-splat-shoot/issues/2)

```
python main.py eval_model_iou mini --modelf=/home/sean/workspace/bev/lift-splat-shoot/pretrain/model525000.pt --dataroot=/mnt/disk/datasets/nuscenes/v1.0-mini
```
```
python main.py viz_model_preds mini --modelf=/home/sean/workspace/bev/lift-splat-shoot/pretrain/model525000.pt --dataroot=/mnt/disk/datasets/nuscenes/v1.0-mini --map_folder=/mnt/disk/datasets/nuscenes/v1.0-mini
```

- visualize input 
```
python main.py lidar_check mini --dataroot=/mnt/disk/datasets/nuscenes/v1.0-mini --viz_train=True
```

- train 
```
python main.py train mini --dataroot=/mnt/disk/datasets/nuscenes/v1.0-mini --logdir=./runs --gpuid=0 --nepochs=1
tensorboard --logdir=./runs --bind_all
```