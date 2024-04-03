# Transformer-PyTorch-Lightning

The goal of this repo is to illustrate how to: 
- use the models from the [Vision Transformer (ViT)](https://github.com/lucidrains/vit-pytorch/tree/main) in [PyTorch Lightning](https://lightning.ai/docs/pytorch/stable/).
- load the trained models in Lightning and do the predictions. 

Therefore, the hyperparameters are not tuned to maximise accuracy. 

This was written in:
```
PyTorch v: 2.1.0
PyTorch Lightning v: 2.2.1
```

#### Data description
Pickle files were generated with ```pandas v 2.1.1```
| Data | Description |
| ------ | ------ |
| train.pkl.gz | Training |
| test.pkl.gz | Testing |
| pred.pkl.gz | Dataset to illustrate loading of trained model and run predictions on |


I used [1d-ViT](https://github.com/lucidrains/vit-pytorch/blob/main/vit_pytorch/vit_1d.py) as an example but this approach can be extended to any other ViT. The provided train/test data are two dimensional time series (250x128) numpy arrays with labels 0 to 1999. Thus this is a time series classification problem.

Lightning will automatically handle the CPU/GPU/TPU, gradients and a lot of other things. So we do not need to specify them at all.
