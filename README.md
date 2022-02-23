# Descriptive-corpus-analysis

## Topic Models for Healthcare 

## Goal

The goal of this project is to perform some explorative analysis of patients' experiences and prepare a preliminary report on what kinds of insights can be generated from this data. The dataset I used is from http://ratemds.com/, a website that posts patient reviews on healthcare professionals. (Please note that input files and certain output files have been excluded for privacy and confidentiality purposes).

Task 1 looks at the corpus collection and corpus descriptive analysis. In this part I conduct some basic descriptive analysis by finding the distribution of the reviews as per gender and sentiment. I also analyze the validity and relevance of the RateMD dataset and compare it to the corpus that a healthcare company would provide. Task 2 delves into LDA and CCLDA analyses of these reviews to produce more insightful analysis of patient reviews.


## Installation

Make sure you have Python3 installed and be sure to use pip install [package_name]  when faced with a package not found error. 
Also make sure to have java installed in order to run the ccLDA in Part 2b

## Usage
Please run this notebook by selecting Run→Run All in the top menu. 
Please note that a private and external CCLDA analysis program was used.

For CCLDA analysis follow these steps after creating your input.txt file in the last cell of the TopicModelling.ipynb file:
1. Open the mftm.16 directory in VSCode or navigate to the corresponding directory in your terminal
2. Place the input_file.txt in the same directory
3. run: javac *.java

### Set 1
3. run: time java LearnTopicModel -model cclda -input input_file.txt -iters 2000 -Z 10
4. run: python topwords_cclda.py input_file.txt.assign > output_10topwords_cclda.txt

### Set 2

5. run: time java LearnTopicModel -model cclda -input input_file.txt -iters 2000 -Z 20
6. run: python topwords_cclda.py input_file.txt.assign > output_20topwords_cclda.txt
