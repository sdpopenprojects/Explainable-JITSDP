# General Introduction

This repository provides the code and datasets used in this article - The effect of data sampling techniques on the interpretation of just-in-time software defect prediction.

### Environment Preparation

- Python	3. 6. 8

```
eli5           0. 13. 0

imblearn       0. 0 

lime           0. 2. 0. 1

numpy          1. 19. 5

optuna         3. 0. 6

pandas         1. 1. 5

shap           0. 41. 0

sklearn        0. 24. 2

statsmodels    0. 12. 2
```

### Repository Structure

- `./Explainable` : Code directory.
  
  - `datasets`：The JIT datasets
  - `demo-global.py`: Python code for conducting comparative experiments on data sampling algorithms to globally explain JIT-SDP models
  - `demo-local.py`：Python code was developed to conduct comparative experiments on data sampling algorithms to locally explain JIT-SDP models
  - `utilities`:  
    - `tuneParameters.py`: The Python code for parameter tuning of a model.
    - `timewiseCV.py`: The Python code for dividing data sets based on time series.
    - `AutoSpearman.py`: The Python code for eliminating metrics that are highly correlated and redundant.
  - `results`：
    - `RQ1` : The results of *Permutation* and *SHAP* methods to globally interpret JIT-SDP models
    - `RQ2` : The top-ranked features of *Permutation* and *SHAP* methods to globally interpret JIT-SDP models
    - `RQ3` : The results of *LIME* and *SHAP* to locally interpret JIT-SDP models
    - `Discuss` : Compaison results between *Permutation* and *SHAP* methods
    -             Compaison results between *LIME* and *SHAP* methods
      
### How to run

- Modify the line in the file `./demo-global.py` , and  `./demo-local.py` , the line are as follows:

  ```R
  # Specify the DIRECTORY path  of dataset
  outpath = "?"
  ```
  
- Run the commands in the terminal.
  
  ```cmd
  $cd your code path
  $python demo-global.py
  $python demo-local.py
  ```
