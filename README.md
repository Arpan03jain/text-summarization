# text-summarization

There are Two different approaches are used for Text Summarization
	1)Extractive Summarization
	2)Abstractive Summarization
	
Extractive Summarization - In Extractive Summarization, we are identifying important phrases or sentences from the original text and extract only these phrases from the text. These extracted sentences would be the summary.

Abstractive Summarization - In the Abstractive Summarization approach, we work on generating new sentences from the original text. The abstractive method is in contrast to the approach that was described above. The sentences generated through this approach might not even be present in the original text.

We are going to focus on using extractive methods. This method functions by identifying important sentences or excerpts from the text and reproducing them as part of the summary. In this approach, no new text is generated, only the existing text is used in the summarization process.

Steps for Implementation
Step 1: The first step is to import the required libraries. There are two NLTK libraries that are necessary for building an efficient text summarizer.


Corpus
A collection of text is known as Corpus. This could be either data sets such as bodies of work by an author, poems by a a particular poet, etc. To explain this concept in the blog, we will be using a data set of predetermined stop words.
Tokenizers
This divides a text into a series of tokens. In Tokenizers, there are three main tokens – sentence, word, and regex tokenizer. We will be using only the word and the sentence tokenizer.
Step 2: Remove the Stop Words and store them in a separate array of words.

Stop Words
Words such as is, an, a, the, for that do not add value to the meaning of a sentence.

Step 3: We can then create a frequency table of the words.

A Python Dictionary can keep a record of how many times each word will appear in the text after removing the stop words. We can use this dictionary over each sentence to know which sentences have the most relevant content in the overall text.


Step 4: Depending on the words it contains and the frequency table, we will assign a score to each sentence.

Here, we will use the sent_tokenize() method that can be used to create the array of sentences. We will also need a dictionary to keep track of the score of each sentence, and we can later go through the dictionary to create a summary.


Step 5: To compare the sentences within the text, assign a score.

One simple approach that can be used to compare the scores is to find an average score of a particular sentence. This average score can be a good threshold.

Apply the threshold value and the store sentences in an order into the summary.
