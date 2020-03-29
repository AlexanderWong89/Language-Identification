# Upskills Language Identification
==============================

Data Science Assignment

## Project Organization
------------

    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── processed      <- data processed from preprocessing notebook exported here
    │   └── raw            <- raw data from assignment
    ├── src                <- Everything was done in notebooks. Exploration. Preprocessing. Classification
    ├── documents          <- assignment document and research paper
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment


--------

## Methodology

### Preprocessing - Creation of Train and Test Sets

1. Train and Test sets are first created by Sentence Tokenizing the text data. Then Using train_test_split (80-20) on the sentences.
2. Standard NLP preprocessing done on train set. Lower casing, removing numbers, punctuation and whitespace, word tokenization. No removal of stopwords, stemming, lemmatization done here because 1. I do no think its so important and 2. I do not know a quick way of validating if the code successfully does this. (I don't understand all the languages haha)
3. Character Trigrams created. Value counts taken and cleaned appropriately. Train Set saved.
4. For the Test Set, I first create a new dataframe where each sentence is a separate row, with a corresponding column for their language
5. Steps 2-3 repeated for Test Set. (without the 'smoothing' steps)

### Classification - Perform Identification on Test Set and prediction on new Input Text

1. Create a function that identifies the language of 1 processed test sample.
2. Perform identification on the test set.
3. Create a function that preprocessing a new text input
4. Create demo for Aurelien to test on a new text input of his choosing

## Results

Almost 100% accuracy in the test set. Errors in Bulgarian and Czech languages (Slavic family).

## Discussion

- Is removing stop words/ stemming/ lemmatizing important? Can explore if it leads to a better model
- Possibly try unigrams and bigrams and compare the models
- During the smoothing step, I could also try the discrete bayes filter, kalman filter, seemed unnecessarily complicated at the time.
- I removed the test samples with less than 50 characters. I should also explore the limits of the model (how few characters required)
- Some research and be done on more accurate language identification on similar languages to improve accuracy.
- explore if relative entropy is the best stat approach.



# Upskills-Language-Identification
