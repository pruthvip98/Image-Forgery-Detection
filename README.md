#Boundary-based Image Forgery Detection by Fast Shallow CNN

https://arxiv.org/abs/1801.06732

The authors of this paper developed a shallow CNN to identify the boundary of the forgery present in an image. They used the Casia v2.0 Image Forgery dataset. https://www.kaggle.com/sophatvathana/casia-dataset

The groundtruth of these images were found here: https://github.com/namtpham/casia2groundtruth

The idea was to extract 32x32 patches with a stride of 10 from the tampered image and corresponding groundtruth image. If the patch from groundtruth image contains 35-65% of tampered region, it will be classified as boundary patch, and non-boundary patch otherwise. Hence, the model will consider 100% tampered or 100% untampered patch as same: non boundary patch, whereas patches with 35-65% tampered region will be considered as boundary patch.

To do this, first I had implemented shallow CNN as described in the paper. Later I implemented CapsuleNet for the same problem.
CapsuleNet: https://arxiv.org/abs/1710.09829
https://towardsdatascience.com/capsule-networks-the-new-deep-learning-network-bd917e6818e8
