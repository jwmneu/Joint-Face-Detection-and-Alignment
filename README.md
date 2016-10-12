Joint-Face-Detection-and-Alignment
==================================

Caffe and Python implementation of Joint Face Detection and Alignment using Multi-task Cascaded Convolutional Networks.

## Set up

Set up environment and copy C++ layer code to Caffe's source code tree.

```
$ export PYTHONPATH=/path/to/Joint-Face-Detection-and-Alignment:$PYTHONPATH
$ export CAFFE_HOME=/path/to/caffe
$ sh layers/copy.sh
```

Compile Caffe following its document.

## Prepare data

Download dataset [WIDER](http://mmlab.ie.cuhk.edu.hk/projects/WIDERFace/), [CelebA](http://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) and [FDDB](http://vis-www.cs.umass.edu/fddb/). Put them in data directory like below.

```
data
├── CelebA
│   └── img_celeba
├── fddb
│   ├── FDDB-folds
│   ├── images
│   │   ├── 2002
│   │   └── 2003
│   └── result
│       └── images
└── WIDER
    ├── wider_face_split
    ├── WIDER_test
    ├── WIDER_train
    └── WIDER_val
```

I have write a matlab script to extract WIDER FACE info from matlab `mat` file to `txt` file.

## Train

Prepare data and train network follow the commands in `train.sh`.

## References

- [A Convolutional Neural Network Cascade for Face Detection](http://www.cv-foundation.org/openaccess/content_cvpr_2015/papers/Li_A_Convolutional_Neural_2015_CVPR_paper.pdf)
- [Joint Face Detection and Alignment using Multi-task Cascaded Convolutional Networks](http://arxiv.org/abs/1604.02878)
- [MTCNN_face_detection_alignment](https://github.com/kpzhang93/MTCNN_face_detection_alignment)
- [py-faster-rcnn](https://github.com/rbgirshick/py-faster-rcnn)
