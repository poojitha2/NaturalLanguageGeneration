# NaturalLanguageGeneration

This project is implemented by Harika Gorijala and Sai Poojitha Chowdary Pallothu under the guidance of Shivanjali Khare as a part of term project for the course Intoduction to Artificial Intelligence - CSCI- 6660 - 02.

## Requirements
We used python 3.10 and jupyter notebbok for the implementation. Operating system is windows. Required libraries for the project are given below:

- numpy
- pandas
- openpyxl
- keras
- tensorflow

You can install the following packages using following command

pip install - <<packageName>>

## Dataset
We used [webNLG](https://gitlab.com/shimorina/webnlg-dataset) data for our project as it is open source and contains lot of RDF Verbalisers.
The WebNLG dataset consists of RDF triples which are mapped to text. The triples take the XML form. These triples are to be mapped to English text which is the lex column in the dataset.

  **Train Models**
We decided on implementing the RNN-LSTM model for our project

## What is NLG?
 
Natural Language Generation is the process of producing text from phrases or sentences.NLG uses structured data to generate text . Some of the applications of NLG are Product and Image descriptions, Customer communications via email and messaging in apps,Analytic Dashboards and Automatic Summarizations, Search results, chatbots, etc. By doing this, we would able to generate text from RDF triples. The end result would be a summary of all the RDF triples which would be more 
easier to read and understand.


## How it works?
 
Our goal with this dataset was to generate text using RDF triples and a RNN LSTM model. To do this, we had to follow a couple of important steps. First, we had to merge all of the 16 WebNLG datasets. Then, we considered all records that have a comment value of ‘good’ and an ID value of ‘Id1’. This ensured that we were only training and testing on unique and valid 
RDF values. Next, we had to preprocess the data. To do this we had to make these changes:
	
1.	Create a 2D array from the mtriple column using the character “|”. 
     a.	Aarhus_Airport | cityServed | "Aarhus, Denmark"
     b.	[“Aarhus_Airport”, “cityServed”, “Aarhus, Denmark”]
2.	Add space at the capital in the 2nd term. This allows us to better replicate the sentence structure of the lex column.
     a.	cityServed -> city Served
3.	Removed unnecessary characters in both columns
     a.	Ex: ,_:@#?!&$]
4.	Convert both columns to lowercase.
5.	Randomize records and then split between train and test
6.	Train the RNN LSTM on the Lex column in the training set.
7.	Generate a sentence from each mtriple by following these steps:
     a.	Generate the next word after the first mtriple value.
     b.	Generate the next word after the second mtriple value.
     c.	Combine the first two generated phrases with the third mtriple in order to form a final sentence.

8.	Run the test set of mtriples through the model and compare the generated sentence to the lex sentence. 
9.	Compute the Bleu Score, F-Score, Precision, and Recall.
10.	Fine-tune the RNN LSTM hyperparameters to optimize the accuracy of the model.
 
## How did you measure performance? 

We measured performance using the Bleu score, Rouge score (F-Score, Precision, and Recall).
Include graphs, equations, pictures, etc. as appropriate
The result of our RNN LSTM is a sentence of generated text. The resultant text is based off of the 3 mtriple values provided by the dataset. We used the beforehand generated text from the lex column of the dataset to train and test our model. Here is an example of our model’s generated text next to the text provided by the Web NLG dataset:
Our Model:
Aarhus airport is located is tirstrup.
Web NLG:
Aarhus airport is located in tirstrup.
As you can see, our model is close to generating text as well as the Web NLG dataset. This is only one example though. Some of our results are the exact same as the provided test data, while some of them differ greatly. On average though, our accuracies are as listed below:
 ![image](https://user-images.githubusercontent.com/52190564/166804959-b7d7d831-bf37-4f23-a82f-cc8e0fa260ef.png)
We achieved this level of accuracy by utilizing the below RNN LSTM:
 ![image](https://user-images.githubusercontent.com/52190564/166805216-dab2fdb6-276c-46db-b36a-b7fbb9bc9ee1.png)
 ![image](https://user-images.githubusercontent.com/52190564/166805304-6bc620de-98b1-4732-80db-b73180ade6f6.png)

With the sentences we generated from this model, we were also able to create a summary of the sentences. You will find this below:
 ![image](https://user-images.githubusercontent.com/52190564/166805392-775a95bb-5fee-4a1a-b0f2-ae72dcf79259.png)

 



