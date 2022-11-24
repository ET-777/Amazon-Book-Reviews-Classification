Amazon Book Reviews Classification
-----------------------

Predict whether or not a book review from amazon is positive or negative using a BERT model. The reviews are also rated by the users and include book information. Dataset is [here](https://www.kaggle.com/datasets/mohamedbakhet/amazon-books-reviews).

Installation
----------------------

### Download the data

* Clone this repo to your computer.
* Create a `Data` folder in the project directory
* Download the data files from Kaggle into the `Data` folder.  
    * You can find the data [here](https://www.kaggle.com/datasets/mohamedbakhet/amazon-books-reviews).
    * You'll need to register with Kaggle to download the data.
* Extract the `.zip` file you downloaded into the `Data` folder.

### Install the requirements
 
* Install the requirements with `anaconda` or with pip using `pip install -r requirements.txt`.
    * Make sure you use Python 3.
    * You may want to use a virtual environment for this.

Usage
-----------------------

* Open `BookReviewsClassification.ipynb` with `Jupyter Notebook`.
* Run the notebook
    * Make sure you are running `tensorflow` with a `GPU`.