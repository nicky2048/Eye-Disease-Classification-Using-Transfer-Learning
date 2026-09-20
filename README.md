# Eye Disease Classification

This project uses transfer learning to classify retinal images across ten eye disease categories.

## Contents

- `Eye Disease Workbook.ipynb`: the training and evaluation notebook

The image dataset is intentionally not included in this repository because of its size. The notebook expects the dataset at:

```text
Eye Disease/data/Original_Dataset/<class folders>/<images>
```
I did not use the augmented dataset due to data leakage concerns.

## Dataset

Download the dataset from [Kaggle](https://www.kaggle.com/datasets/abhinav099802/eye-disease-image-dataset/data), then extract it into the paths above. Do not commit the dataset or `Eye Disease.zip`; both are ignored by Git.

## Running the notebook

Install the Python dependencies imported by the notebook, place the dataset in the expected location, and run `Eye Disease Workbook.ipynb` from the repository root. A CUDA-capable GPU is optional; the notebook falls back to CPU.

21/09 I noticed all the phtos have the little rectangle in the same place so i tried to run it without random rotations to see if it works better, but it performed worse. I also changed the order of augmentation but it performed worse, hence I have left it as it is.
