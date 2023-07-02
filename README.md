# Datasets-Unified

## ImageNet-1K

1. Download the dataset from (https://image-net.org/challenges/LSVRC/2012/2012-downloads.php#images). Training Images (Task 1&2) is the training dataset with the filename ILSVRC2012_img_train.tar (about 138 GB). Validation Images (all tasks) is the validation dataset with the filename ILSVRC2012_img_val.tar (about 6.3 GB). You need to also download the Developement Kit (task 1&2) with the filename ILSVRC2012_devkit_t12.tar.gz and put it in the imagenet folder.
2. We use (https://github.com/pytorch/examples/blob/main/imagenet/extract_ILSVRC.sh) to unzip and process the dataset. This [repo](https://github.com/Jasonlee1995/ImageNet-1K/tree/main) is also useful in pre-processing the dataset and make it ready for PyTorch. It contains the .json file of the class names.

After runnig the script, the directory should be like this: 

```bash
imagenet/train/
  ├── n01440764
  │   ├── n01440764_10026.JPEG
  │   ├── n01440764_10027.JPEG
  │   ├── ......
  ├── ......
  imagenet/val/
  ├── n01440764
  │   ├── ILSVRC2012_val_00000293.JPEG
  │   ├── ILSVRC2012_val_00002138.JPEG
  │   ├── ......
  ├── ......
```
