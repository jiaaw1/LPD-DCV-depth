# Self-supervised Monocular Depth Estimation based on Laplacian Pyramid decoder and Distance Cost Volume

To clearly demonstrate the consistency between the source code and the method described in the paper, 

we provide the correspondence between the source code files and the key components of the algorithm as follows:

networks/resnet_encoder_lp_decoder.py — Defines the configuration of the ResNet encoder and the Laplacian pyramid decoder used in the depth network.

networks/RDCV_transformer.py — Implements the relative distance cost volume using the transformer module.

networks/pose_encoder.py — Contains the encoder of the pose network.

networks/pose_decoder.py — Contains the decoder of the pose network.

In addition, the source code includes detailed comments that highlight the key modules of the algorithm.

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
