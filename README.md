##  [Human Protein Atlas Image Classification](https://www.kaggle.com/c/human-protein-atlas-image-classification) | Capstone Project

The Goal of this project is to develop a model capable of classifying mixed patterns of proteins in  microscope images. And I completed this project in [kaggle kernels](https://www.kaggle.com/kernels), so if you want to recreate this, it will be vary easy to do so. And all the code is well described in the [notebook](https://github.com/githubssd/capstone-project/blob/master/Protein%20Atlas%20Image%20Classification%20with%20fastai.ipynb).
## Data
  This project is a kaggle competition hosted by The Human Protein Atlas and Kaggle.com and data for this project can be found [here](https://www.kaggle.com/c/human-protein-atlas-image-classification/data)
  The data format is two-fold - first, the labels are provided for each sample in  **train.csv**.

The bulk of the data is in the images -  **train.zip**  and  **test.zip**. Within each of these is a folder containing  **four**  files per sample. Each file represents a different filter on the subcellular protein patterns represented by the sample. The format should be  `[filename]_[filter color].png`  for the PNG files, and  `[filename]_[filter color].tif`  for the TIFF files
  ### File descriptions

-   **train.csv**  - filenames and labels for the training set.
-   **sample_submission.csv**  - filenames for the test set, and a guide to constructing a working submission.
-   **train.zip**  - All images for the training set.
-   **test.zip**  - All images for the test set.

### Data fields
-   **Id**  - the base filename of the sample. As noted above all samples consist of four files -  `blue`,  `green`,  `red`, and  `yellow`.
-   **Target** - in the training data, this represents the labels assigned to each sample.

For more insights please take a look at [proposal.pdf](https://github.com/githubssd/capstone-project/blob/master/proposal.pdf) file
## Acknowledgements
The Human Protein Atlas is a Sweden-based initiative aimed at mapping all human proteins in cells, tissues and organs. All the data in the knowledge resource is open access to allow anyone to pursue exploration of the human proteome. In a recent publication, the Human Protein Atlas team has demonstrated the promise of both citizen science and artificial intelligence approaches in describing the location of human proteins in images, however current results are yet to approach expert-level annotations ([Sullivan et al, Nature Biotechnology, Oct 2018](https://www.nature.com/articles/nbt.4225)).
## Project Instructions
### Installation 
Used fastai 0.7.0 and torchvision 0.2.1

```bash
pip install fastai==0.7.0 --no-deps
pip install torch==0.4.1 torchvision==0.2.1
```
for jupyter notebook and kaggle kernels.
```bash
!pip install fastai==0.7.0 --no-deps
!pip install torch==0.4.1 torchvision==0.2.1
```

### Import necessary packages

```python
import os
import pathlib
import pandas as pd
import numpy as np
from sklearn.model_selection import train_test_split
from sklearn.metrics import f1_score
import scipy.optimize as opt
import matplotlib.pyplot as plt
import matplotlib.image as mpimg

from fastai.conv_learner import ConvLearner
from fastai.dataset import get_cv_idxs 
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. And to ask any question, Please use [twitter](https://twitter.com/Rishi_ml) 

## License
[MIT](https://github.com/githubssd/Pytorch-fastai-and-kaggle/blob/master/LICENSE)

