# Machine Learning and Computer Vision Projects

Seven projects by Mehrab Yazdan Manesh. The notebooks cover data preparation, model training, and single-image inference.

| Project | Approach | Notebooks |
| --- | --- | --- |
| Car vs. Bicycle | VGG-style convolutional network with OpenCV image preprocessing | [Training](car-vs-bicycle-training.ipynb), [inference](car-vs-bicycle-inference.ipynb) |
| Car vs. Non-Car | Linear SVM and a dense neural network using resized image pixels | [SVM](car-vs-non-car-svm.ipynb), [neural network](car-vs-non-car-neural-network.ipynb) |
| Human vs. Horse | Residual convolutional network | [Training](human-vs-horse-training.ipynb), [inference](human-vs-horse-inference.ipynb) |
| Human vs. Monkey | ResNet-style image classifier | [Training](human-vs-monkey-training.ipynb), [inference](human-vs-monkey-inference.ipynb) |
| Smile Detection | DenseNet-style facial image classifier | [Training](smile-detection-training.ipynb), [inference](smile-detection-inference.ipynb) |
| COVID-19 Chest X-ray Classification | Experimental dense network using flattened image inputs | [Notebook](chest-xray-classification.ipynb) |
| Maternal Smoking Status Classification | Dense network using tabular features from a maternal and infant health dataset | [Notebook](maternal-smoking-classification.ipynb) |

## Setup

From the repository root, use a Python environment with Jupyter and the project dependencies.

```sh
python -m pip install -r requirements.txt
jupyter notebook
```

For image training notebooks, put the images in one folder per class directly under the `dataset_dir` shown in the notebook. For the tabular experiment, put the expected CSV at `data/babies.csv`. Datasets are supplied separately. For the car vs. non-car examples, set `sample_path` to a sample image before running the last cell.

For the four standalone inference notebooks, download the matching `.keras` checkpoint from [Releases](https://github.com/Mehrab-yazdanmanesh/ai-ml-projects/releases), put it next to the notebook, and set `address` to an input image.

The chest X-ray notebook is an educational image-classification experiment. The notebooks require their source datasets for training, and this repository does not report benchmark or clinical validation results.
