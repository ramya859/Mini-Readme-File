# Mini-Readme-File

Title of the Project : Automated Question Generation using NLP.

Project Idea :

To build a system that generates questions automatically. This system requires the input of a target topic and will generate questions whose answers will be found 
on the paragraph itself. It takes text as input then it summarizes and generates questions using T5 Model. KeyBERT library used for keyword extraction. Distractors
are generated using Wordnet and Sense2Vec approaches. 

Most of the organizations will assign a members to go through the material and manually create MCQ based questions. As we can see it is a lot of time consuming.So 
there is a growing need for a system that can create questions with ease and less amount of time and requires less human effort. This system solves the problem of
manual creation of questions and reduces time consumption and cost.


Modules included in our Project:
 1) Extractive summarization
 2) Keyword Extraction
 3) Question Generation
 4) Generating Distractors

Firstly, we loaded the raw text and extractive summarization is applied on the text.

**Extractive summarization**
It simply means picking out the important sentences as it is from the paragraph and form a summary. For extractive summarization we have used T5 Transformer model. 
Then after extractive summarization you can perhaps paraphrase the sentences that we got in summarization. It will generate output as summarized and precised text.
For summarization we have taken Base-T5 model from Huggingface Transformer. One thing is that we dont need to train anything because the Base model that is provided 
by Google on hugging face already has summarization.  

**Keyword Extraction**
Keyword extraction means extracting the keywords from the summarised text i.e; taking summarized text as input which we got in the previous stage to key BERT algorthm and it will extract the keywords. Key Bert algorithm is very efficient and gives better performance compared to other algorithms. Key BERT extract grammatically correct keyphrases that are most similar to a document.  

**Question Generation**
Once you extract those keywords so with summarised text and those extracted keywords as input given to T5 Transformer Model and it automatically generates questions.
The T5 (Text-To-Text Transfer Transformer) Model uses text-to-text approach where the input and output are always text strings. Every task including translation, question answering, and classification is cast as feeding the model text as input and training it to generate some target text.

**Generating Distractors**
Distractors are the wrong choices to Multiple Choice questions. So, for generating distractors we used Wordnet and Sense2Vec approaches. Correct answer will be the keyword itself. Distractors will be generated related to the keyword considered. Wordnet is a lexical database of semantic relations between words in more than 200 languages. Sense2Vec is an incredible tool to get synonyms and correlations, given a keyword. 

For example, if a given multiple choice question has Barack Obama as the correct answer then we need to generate wrong choices (distractors) like George Bush, Bill Clinton, Donald Trump, etc.  in order to effectively filter near-duplicates, convert the original answer word as well as each of the words from similar word results 
in sense2vec to a vector using Sentence Transformers.

**Gradio UI Visualization**
We have implemented our model in Gradio UI. It is an open-source Python library that is used to build machine learning and data science demos and web applications. 
It allows you to develop an easy-to-use customizable component demo for your machine learning model that anyone can use anywhere. 

And the accuracy of the distractor generated is reasonably high. This system not only helps teachers with E-assessments but also helps students who are preparing for competitive exams. Students can test their ability to solve the questions and can also check their understanding of the concepts.

