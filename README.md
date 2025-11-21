# Self-supervised Monocular Depth Estimation based on Laplacian Pyramid decoder and Distance Cost Volume

This repository provides the implementation of our paper"Self-supervised Monocular Depth Estimation based on Laplacian Pyramid decoder and Distance Cost Volume".
We ensure that the key algorithmic components, network architecture, training strategy, and evaluation protocol strictly follow the descriptions in the paper.
## Implementation Notes on Novel Contributions

To help readers locate the implementations of our novel components, we have added detailed comments in the corresponding source files:

Innovation 1: Implemented and annotated in networks/resnet_encoder.py.

Innovation 2: Implemented and annotated in networks/RDCV_transformer.py.

## Training

To train on KITTI, run:

```bash
python train.py ./args_files/train_640_192.txt
```
For instructions on downloading the KITTI dataset, see [Monodepth2](https://github.com/nianticlabs/monodepth2)

## Evaluation

To evaluate a model on KITTI, run:

```bash
python evaluate_depth_config.py ./args_files/eval_640_192.txt
```

Make sure you have first run `export_gt_depth.py` to extract ground truth files.

## Inference with your own iamges

```bash
python test_simple.py --image_path --model_name
```
