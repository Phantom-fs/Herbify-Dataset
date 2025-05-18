# Herbify Dataset

This repository contains the dataset for herb classification and recognition, named **Herbify**. The dataset is derived from two datasets and is manually cleaned, with further improvements and processing. The dataset is designed to facilitate research in the field of herb (plant) classification and recognition using deep learning techniques.

#### Links:

- **[Code](https://github.com/Phantom-fs/Herbify-Dataset)**

## Table of Contents

- [Dataset](#dataset)
- [Getting Started](#getting-started)
- [Citation](#citation)
- [License](#license)

## Dataset

The dataset consists of images of **91** different herbs, with a total of **6,104** images. The structure of the dataset is as follows:

```text
Herbify-Dataset/
    Scientific name (Common name)/
        image1.jpg
        image2.jpg
        ...
    Scientific name (Common name)/
        image1.jpg
        ...
    ...
```

Images within the Herbify dataset vary in spatial resolution from **103 × 94** pixels to **4236 × 4447** pixels, with an average resolution of approximately **1267 × 1135** pixels. Each species class contains between **7** and **163** images, with an average of **67** images per class.

- **Input Parameters:**
  - **Image:** The images of the herbs (JPEG format).
  - **Label:** The labels are in the format 'scientific names (common names)' of the herbs (folder names).
- **Output Parameter:**
  - **Classification:** The predicted class (herb name) based on the input image.

### Download

The dataset is also available to be downloaded from the following sites:

- **Kaggle:** Coming soon
- **HuggingFace:** Coming soon

## Getting Started

To use this dataset for your research or project:

1. **Clone the repository:**

   ```sh
   git clone https://github.com/Phantom-fs/Herbify-Dataset.git
   ```

2. **Download the dataset:**
   - Download from Kaggle or HuggingFace (links above), or use the files in this repository.

3. **Dataset structure:**
   - Each folder is named after a herb (scientific name (common name)) and contains images of that herb.

4. **Usage example (Python):**

   ```python
   import os
   from PIL import Image

   dataset_path = 'Herbify-Dataset'
   for herb in os.listdir(dataset_path):
       herb_folder = os.path.join(dataset_path, herb)
       if os.path.isdir(herb_folder):
           for img_file in os.listdir(herb_folder):
               img_path = os.path.join(herb_folder, img_file)
               img = Image.open(img_path)
               # process image
   ```

    Check the **[Code](https://github.com/Phantom-fs/Herbify-Dataset)** for detailed usage.

## Citation

If you are using the dataset, please cite using this BibTeX:

```bibtex

```

## Derived Dataset Citations

### DIMPSAR

```bibtex
@article{BR2023109388,
    title = {DIMPSAR: Dataset for Indian medicinal plant species analysis and recognition},
    journal = {Data in Brief},
    volume = {49},
    pages = {109388},
    year = {2023},
    issn = {2352-3409},
    doi = {https://doi.org/10.1016/j.dib.2023.109388},
    url = {https://www.sciencedirect.com/science/article/pii/S2352340923005000},
    author = {Pushpa {B R} and N. Shobha Rani},
    keywords = {Plant classification, Leaf images, Whole plant images, Mobile captured images, Plant/leaf analysis},
}
```

### DeepHerb

```bibtex
@ARTICLE{9551957,
    author={Roopashree, S. and Anitha, J.},
    journal={IEEE Access},
    title={DeepHerb: A Vision Based System for Medicinal Plants Using Xception Features},
    year={2021},
    volume={9},
    number={},
    pages={135927-135941},
    keywords={Feature extraction;Biomedical imaging;Deep learning;Support vector machines;Neural networks;Transfer learning;Convolutional neural networks;Bayesian optimization;computer vision;deep learning;medicinal plants;support vector machine;transfer learning;Xception},
    doi={10.1109/ACCESS.2021.3116207}
}
```

### Dataset Links

- **DIMPSAR:** [DIMPSAR Dataset](https://data.mendeley.com/datasets/748f8jkphb/2)
- **DeepHerb:** [DeepHerb Dataset](https://data.mendeley.com/datasets/nnytj2v3n5/1)

This dataset is intended for research purposes only. If you use this dataset in your research, please also cite the original sources of the datasets used to create it. 

## License

This project is licensed under:

[Creative Commons Attribution-NonCommercial 4.0 International License][cc-by-nc].

[![CC BY-NC 4.0][cc-by-nc-shield]][cc-by-nc]

[![CC BY-NC 4.0][cc-by-nc-image]][cc-by-nc]

[cc-by-nc]: https://creativecommons.org/licenses/by-nc/4.0/
[cc-by-nc-image]: https://licensebuttons.net/l/by-nc/4.0/88x31.png
[cc-by-nc-shield]: https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg

See the [LICENSE](LICENSE) file for details.