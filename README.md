# Gradient Descent and BCGD Methods with an Application on Rice Seeds Classification

> Semi-supervised learning applied to rice seeds classification, using Gradient Descent and Block Coordinate Gradient Descent (BCGD) methods for optimization.

<p align="center">
<img src="https://github.com/alecruces/OptiRice/assets/67338986/506491de-f0b0-4d6d-b6b1-a67f17ae32c9" alt="opt2" style="width:400px;height:auto;"/>
</p>


##  Keywords
Optimization Methods, Semi-Supervised Learning, Rice Seeds Classification

---

## Table of Contents

1. [About the Project](#about-the-project)
2. [Key Features](#key-features)
3. [Key Results](#key-results)
4. [Data Overview](#data-overview)
5. [Methodology](#methodology)
6. [Screenshots and Graphs](#screenshots-and-graphs)
7. [Technologies Used](#technologies-used)
8. [Setup & Installation](#setup--installation)
9. [Usage](#usage)
10. [Contributing](#contributing)
11. [License](#license)
12. [Contact](#contact)

---

### About the Project

This project explores semi-supervised learning using optimization methods for classifying rice seed types. We apply three optimization methods—Gradient Descent, Randomized Block Coordinate Gradient Descent (BCGD), and Gauss-Southwell BCGD—to both a synthetic dataset and a real-world rice seeds dataset. By minimizing an objective function, the study demonstrates how labeled data can guide label predictions for unlabeled instances, with performance measured in accuracy and computation time.

### Key Features

- **Semi-Supervised Learning**: Efficient label prediction for unlabeled data using a small set of labeled data.
- **Optimization Techniques**: Implementation of three optimization methods with convergence analysis and performance comparison.
- **Real-World Application**: Classification of rice seeds based on morphological attributes.

### Key Results

- **Convergence Behavior**: Gradient Descent converges in fewer iterations, while Gauss-Southwell BCGD is the fastest in terms of computational time.
- **Accuracy**: Achieved approximately 70% accuracy on true labels for the real rice seeds dataset, indicating effective label assignment.
- **Similarity Measure**: Exponential similarity (RBF kernel) yielded better performance compared to Euclidean distance for clustering.

### Data Overview

This project utilizes a synthetic dataset and a real-world rice seed dataset:

- **Rice Type Data Set**: [Rice Type Classification Dataset on Kaggle](https://www.kaggle.com/datasets/mssmartypants/rice-type-classification)  
  Contains attributes of rice grains, including area, perimeter, axis lengths, eccentricity, and convex area, used for classification between Jasmine and Gonen rice types.

### Methodology

The following optimization techniques were applied:

- **Gradient Descent**: Basic optimization technique with convergence based on gradient computation.
- **BCGD with Randomized Rule**: Coordinates updated based on random selection of blocks.
- **BCGD with Gauss-Southwell Rule**: Blocks are selected based on the direction of maximum gradient magnitude.

Additional methodology aspects include:

- **Similarity Measures**: RBF kernel used for calculating similarity weights between data points.
- **Stopping Criteria**: Convergence is determined by either a set iteration limit or the magnitude of the gradient.

### Screenshots and Graphs

1. **Distribution of Synthetic Data (Scatter Plot)**  
   Visualization of labeled and unlabeled points before applying the optimization methods.

   <p align="center">
   <img width="416" alt="optirice_1" src="https://github.com/user-attachments/assets/cb886d74-bc3e-4b38-9331-c680778b6978">

  </p>
  
Distribution of examples for the synthetic data set before appliying optimization algorithms. Symbol + denotes unlabeled data, dotes denotes labeled data (two classes: yellow and purple.)

2. **Accuracy vs. Iterations for Synthetic Data (Line Chart)**  
   Comparison of accuracy across iterations for each optimization method on the synthetic dataset.

   <p align="center">
    <img width="633" alt="optirice_acc" src="https://github.com/user-attachments/assets/6a66f6f5-87cd-40fa-9544-0c45c8a9ba7f">
   </p>

 Accuracy as a function of iteration number based on continuous values (left) and on loss function (right).


3. **Distribution of Rice Seeds Data (Scatter Plot)**  
   Shows the labeled and unlabeled distribution of rice seeds, with attributes such as eccentricity and perimeter.

   <p align="center">
    <img width="425" alt="optirice_real_after" src="https://github.com/user-attachments/assets/7db177d3-443a-4f99-8961-3e1500def193">

   </p>
Distribution of examples for the real data set after applying Gradient Descent algorithm. Symbol + denotes the predicted unlabeled data (now labeled with a class), dotes denotes the true unlabeled data.

4. **Accuracy and Loss over Time (Line Charts)**  
   Shows accuracy as a function of CPU time for rice seed datasets, and loss

   <p align="center">
    <img width="642" alt="optirice_acc_cpu_real" src="https://github.com/user-attachments/assets/1659e5f8-1130-4166-a8ed-f8be3e68c755">
   </p>

 Accuracy as a function of CPU time based on continuous values (left) and on loss function (right) with a time window of 10,000 ms.
 
   <p align="center">
    <img width="638" alt="loss_real" src="https://github.com/user-attachments/assets/e4313173-fca7-48ef-b5e4-5d7c873d5d5c">
   </p>

   Loss as a function of iteration number (left) and as a function of CPU time (right) with time window of 10,000 ms.

### Technologies Used

> 🛠️ Highlighting essential tools and libraries.

- ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white): Main programming language.
- **NumPy** and **Pandas**: Data manipulation and processing.
- **Matplotlib**: Visualization of data distribution, accuracy, and loss trends.

### Setup & Installation

Clone the repository and install dependencies to replicate the study:

```bash
# Clone the repository
git clone https://github.com/username/OptiRice.git
```


# Navigate to the project directory
cd OptiRice

# Install dependencies
pip install -r requirements.txt

### Usage

The repository includes the following files:

- **`code.ipynb`**: Jupyter notebook with the complete workflow, from data loading to optimization and performance evaluation.
- **`Report.pdf`**: Detailed report covering the methodology, convergence analysis, and findings.

To run the project, open `code.ipynb` in Jupyter Notebook or view it on [nbviewer](https://nbviewer.org/github/alecruces/OptiRice/blob/main/code.ipynb).

### Contributing

Contributions are welcome! Please refer to the contributing guidelines for more details.

