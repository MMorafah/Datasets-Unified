# Datasets-Unified

### ImageNet-1K

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
### [ImageNet-A](https://github.com/hendrycks/natural-adv-examples)

We followed this [repo](https://github.com/mlfoundations/model-soups/blob/main/datasets.md).

```bash
wget https://people.eecs.berkeley.edu/~hendrycks/imagenet-a.tar
tar xvf imagenet-a.tar
rm imagenet-a.tar
```
### [ImageNet-R](https://github.com/hendrycks/imagenet-r)

We followed this [repo](https://github.com/mlfoundations/model-soups/blob/main/datasets.md).

```bash
wget https://people.eecs.berkeley.edu/~hendrycks/imagenet-r.tar
tar xvf imagenet-r.tar
rm imagenet-r.tar
```

### [ImageNet Sketch](https://github.com/HaohanWang/ImageNet-Sketch)
We followed this [repo](https://github.com/mlfoundations/model-soups/blob/main/datasets.md).

Download links:
- from [Google Drive](https://drive.google.com/open?id=1Mj0i5HBthqH1p_yeXzsg22gZduvgoNeA)
- from [Kaggle](https://www.kaggle.com/wanghaohan/imagenetsketch)

### [ImageNet V2](https://github.com/modestyachts/ImageNetV2)
We followed this [repo](https://github.com/mlfoundations/model-soups/blob/main/datasets.md).

```bash
wget https://s3-us-west-2.amazonaws.com/imagenetv2public/imagenetv2-matched-frequency.tar.gz
tar -xvf imagenetv2-matched-frequency.tar.gz
rm imagenetv2-matched-frequency.tar.gz
```

### [ObjectNet](https://objectnet.dev/)
We followed this [repo](https://github.com/mlfoundations/model-soups/blob/main/datasets.md).

```bash
wget https://objectnet.dev/downloads/objectnet-1.0.zip
unzip objectnet-1.0.zip
rm objectnet-1.0.zip
```

### [iNaturalist](https://github.com/visipedia/inat_comp/tree/master)
We used this [page](https://github.com/visipedia/inat_comp/tree/master/2017) to download the dataset. We downloaded the 2017 version. Then you need to unzip it to a new foloder called 2017 for the PyTorch data loader. Then you need to also download the annotation file for it.

For PyTorch build-in Dataloader it should be like this: 
```bash
2017/
  ├── Aminat
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
Put the traion2017.json and val2017.json in the 2017 folder itself. 
For using the dataloader from other than PyTorch, you need to have the foloder train_val_images exist. Use the this [repo](https://github.com/macaodha/inat_comp_2017/blob/master/ignat_loader.py) or this [repo](https://github.com/macaodha/inat_comp_2018/blob/master/inat2018_loader.py) for manual dataloader.

