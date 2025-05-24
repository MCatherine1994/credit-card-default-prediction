# DSCI_573_lab4_JJJC Credit Card Default Prediction

DSCI 573 lab4 for Group: **Jenson Chang, Catherine Meng, Jingyuan Wang, Zejiao Zeng**

A machine learning classification project predicting credit card default. This project follows the complete ML workflow—starting with exploratory data analysis (EDA), followed by feature engineering, feature selection and importance analysis, model comparison, and hyperparameter optimization. It evaluates and compares the performance of **Logistic Regression**, **Random Forest**, **LightGBM**, and **XGBoost** models. Results are presented via a Quarto website.

This project addresses a binary classification problem: predicting whether a credit card client will default on their payment in the next month. It uses the [Default of Credit Card Clients Dataset](https://www.kaggle.com/uciml/default-of-credit-card-clients-dataset), which contains 30,000 records and 24 features, including demographic information, payment history, and billing amounts from April to September 2005.

The target variable is default.payment.next.month, indicating whether the client defaulted. The remaining features provide monthly financial and repayment data that help inform this prediction task.

This dataset was originally featured in a [research study](https://www.sciencedirect.com/science/article/pii/S0957417407006719) comparing classification models for default prediction. Results in this project may be compared against findings from the paper.


## Setup Quarto Website

### Convert the jupyter notebook to the quarto page

```{bash}
quarto convert project.ipynb -o project.qmd
```

Update the name and display_name in `project.qmd` to "python3"

### Render the qmd file

```{bash}
quarto render project.qmd
```

### Hosting project.html on GitHub Pages

Move rendered files there so GitHub Pages can find them:

```{bash}
mkdir docs
mv project.html docs/
mv project_files docs/
```

Enable GitHub Pages:

- Go to GitHub repository page
- Click Settings → Pages
- Under Source, select:
    - Branch: main (or your default branch)
    - Folder: /docs
    - Click Save