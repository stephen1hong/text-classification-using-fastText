# text-classification-using-fastText

0) install fastText (if not installed)
  $git clone https://githb.com/facebookresearch/fasttext.git
  $ cs fasttext
  $ make

1) download dataset
- from Yelp’s 4.7 millon user reviews
  (help.com/dataset/download)

2) preprocessing of datsets
   -fastText requires a text file with each piece of text on a line by itself, format something like below:

   __label__5 This restaurant is great!
   
   __label__1 This restaurant is terrible 

3) Produce  a Training set and a Test set
  
4) train the model
$./fasttext supervised -input fasttext_dataset_training.txt -output reviews_model

5) test the model
$./fasttest test reviews_model.bin fasttext_dataset_test.txt

6) make the model more accurate by ngram size
$/fasttext supervised -input fasttext_dataset_training.txt -output reviews_model_ngrams -wordNgrams 2
