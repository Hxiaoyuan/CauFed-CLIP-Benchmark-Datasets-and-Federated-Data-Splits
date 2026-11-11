# Dataset Download Guide

This README provides download links and source references for five public datasets used in **Identifiable Causal Disentanglement for Federated Vision-Language Learning**.

The links point to releases maintained by the original dataset providers or to the explicitly identified repository records. This README is an access guide; the datasets remain distributed through those external sources.

## Dataset overview

| Dataset | Classes | Domains or standard split | Download |
| --- | --- | --- | --- |
| PACS | 7 | Art Painting, Cartoon, Photo, Sketch | [Dataset folder](https://drive.google.com/drive/folders/0B6x7gtvErXgfUU1WcGY5SzdwZVk?resourcekey=0-2fvpQY_QSyJf2uIECzqPuQ&usp=sharing) |
| CIFAR-10 | 10 | 50,000 training images; 10,000 test images | [Python archive](https://cave.cs.toronto.edu/kriz/cifar-10-python.tar.gz) |
| OfficeHome | 65 | Art, Clipart, Product, Real-World | [Dataset archive](https://drive.google.com/file/d/0B81rNlvomiwed0V1YUxQdC1uOTg/view?resourcekey=0-2SNWq0CDAuWOBRRBL7ZZsw&usp=sharing) |
| Modern Office-31 | 31 | Amazon, Webcam, DSLR, Synthetic in the downloadable package | [Dataset archive](https://drive.google.com/file/d/1p7ecv9kP3YbmdiY49vSjTaG0Aw51n26x/view?usp=sharing) |
| CIFAR-100 | 100 | 50,000 training images; 10,000 test images | [Python archive](https://cave.cs.toronto.edu/kriz/cifar-100-python.tar.gz) |

## 1. PACS

PACS is a domain generalization benchmark with 9,991 images across seven classes and four visual domains.

- **Official project page:** [Deeper, Broader and Artier Domain Generalization](https://dali-dl.github.io/project_iccv2017.html)
- **Download:** [PACS dataset folder on Google Drive](https://drive.google.com/drive/folders/0B6x7gtvErXgfUU1WcGY5SzdwZVk?resourcekey=0-2fvpQY_QSyJf2uIECzqPuQ&usp=sharing)
- **Original paper DOI:** [10.1109/ICCV.2017.591](https://doi.org/10.1109/ICCV.2017.591)

The official download page provides the dataset and the original train/validation splits. To reproduce CauFed-CLIP experiments, follow the domain selections and federated partition settings described in the manuscript and supplementary material.

## 2. CIFAR-10

CIFAR-10 contains 60,000 color images of size 32 × 32 pixels in ten classes, with 50,000 training images and 10,000 test images.

- **Original dataset homepage:** [CIFAR-10 and CIFAR-100](https://cave.cs.toronto.edu/kriz/cifar.html)
- **Download:** [cifar-10-python.tar.gz](https://cave.cs.toronto.edu/kriz/cifar-10-python.tar.gz)
- **Dataset DOI (UCI record):** [10.24432/C5889J](https://doi.org/10.24432/C5889J)
- **UCI record:** [CIFAR-10](https://archive.ics.uci.edu/dataset/691/cifar+10)
- **Alternative archive:** [CIFAR-10 & CIFAR-100 on Zenodo](https://zenodo.org/records/10089977)
- **Python archive MD5:** `c58f30108f718f92721af3b95e74349a`

The UCI DOI identifies the CIFAR-10 repository record. The original dataset homepage provides the downloadable archives and the recommended technical-report citation.

## 3. OfficeHome

OfficeHome, also written as Office-Home, is an object recognition benchmark with 65 categories across four domains: Art, Clipart, Product, and Real-World.

- **Official dataset homepage:** [Office-Home Dataset](https://www.hemanthdv.org/officeHomeDataset.html)
- **Download:** [OfficeHomeDataset_10072016.zip on Google Drive](https://drive.google.com/file/d/0B81rNlvomiwed0V1YUxQdC1uOTg/view?resourcekey=0-2SNWq0CDAuWOBRRBL7ZZsw&usp=sharing)
- **Original paper DOI:** [10.1109/CVPR.2017.572](https://doi.org/10.1109/CVPR.2017.572)

The DOI refers to *Deep Hashing Network for Unsupervised Domain Adaptation*, the paper introducing the dataset. Please consult the dataset homepage for its use conditions and citation instructions.

## 4. Modern Office-31

Modern Office-31 updates Office-31 with a refurbished Amazon domain and a synthetic domain. The downloadable package contains Amazon, Webcam, DSLR, and Synthetic data, totaling 7,210 images across 31 classes.

- **Official project repository:** [tringwald/Adaptiope](https://github.com/tringwald/Adaptiope#modern-office-31)
- **Download:** [Modern-Office-31.zip on Google Drive](https://drive.google.com/file/d/1p7ecv9kP3YbmdiY49vSjTaG0Aw51n26x/view?usp=sharing)
- **Original paper DOI:** [10.1109/WACV48630.2021.00015](https://doi.org/10.1109/WACV48630.2021.00015)
- **Archive SHA-256:** `da02da26ec456def6af39d32c794070cb51a3b5696489172f70f69f2da2f1a63`

Select the **Modern Office-31** download on the project page. The separately listed **Adaptiope** download is a different benchmark with 123 classes. The dataset authors' original Modern Office-31 experiments use Amazon, Synthetic, and Webcam; the provided archive additionally includes DSLR.

## 5. CIFAR-100

CIFAR-100 contains 60,000 color images of size 32 × 32 pixels in 100 classes, with 50,000 training images and 10,000 test images. Its fine-grained classes are grouped into 20 superclasses.

- **Original dataset homepage:** [CIFAR-10 and CIFAR-100](https://cave.cs.toronto.edu/kriz/cifar.html)
- **Download:** [cifar-100-python.tar.gz](https://cave.cs.toronto.edu/kriz/cifar-100-python.tar.gz)
- **Alternative download:** [CIFAR-100 Python archive on Zenodo](https://zenodo.org/records/10089977/files/cifar-100-python.tar.gz?download=1)
- **Dataset archive DOI:** [10.5281/zenodo.10089977](https://doi.org/10.5281/zenodo.10089977)
- **Python archive MD5:** `eb9058c3a382ffc7106e4002c42a8d85`

The Zenodo DOI identifies the record titled **CIFAR-10 & CIFAR-100**, which contains both datasets. Select `cifar-100-python.tar.gz` for CIFAR-100.

## Reproduction notes

- The links above provide upstream dataset releases. Use the preprocessing, source/target domain selections, client partitions, and evaluation protocols specified in the manuscript and supplementary material when reproducing CauFed-CLIP.
- The CIFAR-10 and CIFAR-100 archives listed here contain the clean datasets. CIFAR-10-C and CIFAR-100-C are separate corruption benchmarks and require separate downloads for corruption experiments.
- If a download URL changes, use the corresponding official project page or repository record to locate the current release.
