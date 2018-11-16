Passion Power Project
====

This is called a 'spec' (specification), and it explains what we are going to do for the coding portion of this project. First, we will be going over some background knowledge for those with less or no experience, so this club can actually support quantitative projects in the future.

## What is Git? 
The code we will be writing will be stored on GitHub in this [repository](https://github.com/whalish/Voyager). This helps with version control and shared access (i.e. store all past and present versions of code that we can all access and modify). This is done with the intention of leaving the code for teams to use in the future. If you don't know git, simply write the code on your local text editors and send the files to me. If you do know git, make your changes in a branch and submit a pull request to me. Never commit to master.

## What is an API?
![](https://i.imgur.com/oeBoRnP.jpg)

API stands for Application Programming Interface. Essentially, an API consists of a bunch of building blocks that a programmer can use to build whatever it is they want to build. The company that implements the API (usually in either a library or network context), in this case Google, hides the actual implementation from the user (either for sake of simplicity or because they want to keep it secret). In our case, we want to use Google's Sentiment Analyzer. The actual code is probably worth millions, and is definitely not private. However, Google provides a public API (a server aka Google Cloud API) that acts as the middle man, and we send the API requests which in turn executes a bunch of mysterious shit and returns to us what we need. We then take that building block and use it as a variable in the rest of our code.

## What is Natural Language Processing?

**Business majors pay attention so you don't end up on I can handle the business side**
![](https://i.imgur.com/7Ls4gB3.png)

AI - making programs that **appear** to **act** rational (e.g. Q-Learning, Minimax, think Roomba)

ML - AI that is not explicitly told to do something, but learns it itself either with (e.g. Regression, SVMs, Decision Trees, LDA/QDA) or without (e.g. K-Means, PCA, SVD) supervision. Feed in LOTS of data.

DL - Evolution of ML that learns based on data representations, learns things that are "deep" and hard to explain (Neural Nets, CNN, RNN).

NLP - Programs that can understand language. Nowadays, mostly uses Deep Learning (LSTM).

The Sentiment Analyzer is an already trained DL model for NLP purposes (probably a super fancy LSTM). It will take a paragraph and do two things. First of all, it will identify all the entities in the sentence (e.g. "The air sucks" -> ["air"]). Not sure if entities are just nouns - probably some subtle distinctions. Then it will assign sentiment to see how people feel about it (e.g. {"air", "-1", ".8"}).

## Tasks
We have three parts to this task. It will be implemented in Python (YAY 61A peeps).

1. **Sentiment Analysis**. We will read in whatever survey text we are trying to analyze, and we will assume input format to be excel sheet. The instructions for how to do this are [here](https://cloud.google.com/natural-language/docs/sentiment-tutorial). Note that you need to first make a Google Cloud account and set up authentication (honestly will be the longest part probs). We need to read through the excel sheet one by one, request each entry to be analyzed by the Google Cloud API, and then store the results.

2. **Voyager Analysis**. Given all the results per survey text, we need some way of aggregating them. Possibilities include: sums, averages, average magnitude, L1 norm, L2 Norm, etc. After doing this we can return the most important entities and how they are viewed.

3. **Testing**. Create some example sentences, call the API we are defining above, and make sure the output makes sense. Short part.


My intention is to not write any code, I'm so tired of coding pls help me out. Honestly there isn't a TON of code to be written, if we finish this early and people still want stuff to do we can expand our library to include segmentators and plotters and linear regression and all of that good stuff (maybe even train our own nn).
