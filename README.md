Amazon Book Reviews Classification
-----------------------

Deep network for predictiong whether or not a book review from amazon is positive or negative using the BERT model. The text reviews are cleaned before using the BERT preprocessor. The dataset contains 3 million reviews with user, and book information. A rating from 1-5 is also given for each review. This feature is converted into binary values to classify the reviews. Dataset is [here](https://www.kaggle.com/datasets/mohamedbakhet/amazon-books-reviews). You can see the data processing, model, code, and full explanations in the `BookReviewsClassification.ipynb` notebook above.

Quick Overview
----------------------

Before trainig the model, the text was cleaning by removing the following:

* stopword
* punctuation
* numbers
* single characters

<p align="center">
<br />
Original text
<br />
<br />
I don't care much for Dr. Seuss but after reading Philip Nel's book I changed my mind--that's a good testimonial to the power of Rel's writing and thinking. Rel plays Dr. Seuss the ultimate compliment of treating him as a serious poet as well as one of the 20th century's most interesting visual artists, and after reading his book I decided that a trip to the Mandeville Collections of the library at University of California in San Diego was in order, so I could visit some of the incredible Seuss/Geisel holdings they have there.There's almost too much to take in, for, like William Butler Yeats, Seuss led a career that constantly shifted and metamoprhized itself to meet new historical and political cirsumstances, so he seems to have been both a leftist and a conservative at different junctures of his career, both in politics and in art. As Nel shows us, he was once a cartoonist for the fabled PM magazine and, like Andy Warhol, he served his time slaving in the ad business too. All was in the service of amusing and broadening the minds of US children. Nel doesn't hesitate to administer a sound spanking to the Seuss industry that, since his death, has seen fit to license all kinds of awful products including the recent CAT IN THE HAT film with Mike Myers. Oh, what a cat-astrophe!The book is great and I can especially recommend the work of the picture editor who has given us a bounty of good illustrations.
<br />
<br />
<br />
Text after cleaning
<br />
<br />
dont care much dr seuss reading philip nels book changed mindthats good testimonial power rels writing thinking rel plays dr seuss ultimate compliment treating serious poet well one th centurys interesting visual artists reading book decided trip mandeville collections library university california san diego order could visit incredible seussgeisel holdings theretheres almost much take like william butler yeats seuss led career constantly shifted metamoprhized meet new historical political cirsumstances seems leftist conservative different junctures career politics art nel shows us cartoonist fabled pm magazine like andy warhol served time slaving ad business service amusing broadening minds us children nel doesnt hesitate administer sound spanking seuss industry since death seen fit license kinds awful products including recent cat hat film mike myers oh catastrophethe book great especially recommend work picture editor given us bounty good illustrations
<br />
<br />
<br />
<br />
</p>

The model is constructed with the functional API, calling the BERT processor and encoder, and additionally, a dropout layer to reduce overfitting. The output Dense layer uses a sigmoid activation.

<p align="center">
<br />
Model
<br />
<br />
<img src="https://github.com/ET-777/Amazon-Book-Reviews-Classification/blob/master/images/model.jpg" heigth="60%" width="60%"/>
<br />
<br />
<br />
</p>

Results
----------------------

The model was trained for 3 epochs with a BinaryCrossentropy loss function and adam optimizer. Data was also split by 30% for testing.
<br /><br />
 Data | Loss | Accuracy
------------ | ------------- | -------------
Training | 0.56 | 0.71
Validation | 0.52 | 0.75

<br /><br />
The loss scores are very close, this means the model did not overfit the training data and generalize well as seen with the accuracy scores. Both scores perform well, and the validation data did better than the training data. It's a decent model, but transfer learning with other models might give better results.
<br /><br />

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
