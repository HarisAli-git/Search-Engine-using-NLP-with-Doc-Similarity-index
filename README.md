# Search-Engine-using-NLP-with-Doc-Similarity-index

### Abstract:
Natural language processing (NLP), one of the latest innovations and sub-branches of artificial intelligence, is an area that is continuously on-edge and bringing state-of-the-art research and development. To dive in further, NLP is a sub-branch of computational science and artificial intelligence that handles language data between machines, humans, and data sources such as text and sound. NLP refers to when machines express inferences by understanding human language and deriving the meanings it derives from it. As in machine learning, computers are taught at a level that can understand human language. 
Today, we all know about the influence of search engine in our lives. But now the modern world is going towards Search Engine using NLP which helps us to make document summarization, search the occurrences of a particular word, similarity between the two documents etc. 
Our project exactly finds the same to build a search engine using NLP. The data structures help to record relations between documents and words, search for information within the documents, and compare documents to each other to group them. Our strategy is to read files of text documents, converts them into machine representations using a vector-space model, and then computes similarities between documents using a given similarity measure. The program computes as its final result a document-document incidence matrix that shows the similarity of each document to each other. The incidence matrix must be printed to the screen. The results of this thesis showed that integrating NLP in a search engine has the potential of increasing the focus of a search and to more accurately identify the context of documents.
Introduction
In this project, we are building a search engine. There was a need for search engine which can search for occurrences of words in a document. For example, in an article how many time the word arrow occurs. So our project will solve this problem. We will first tokenize the document. For example, in an article all the words are separated with spaces so our program will separate these words. Then we will invert the index and this inversion will be done by two different methods; first will be with hash tables and dictionary and second one will be without hash tables or dictionary. After that, all the indexes will be read and the occurrences will be found out.
In addition to this our project will also find the similarity index. It is a well-known problem that up to what extent two or more documents match with each other. So we are using Natural Language Processing (NLP) to find the similarity index of two or more documents. Like for example, if there are two different articles on military of Pakistan then the input of our application would be these two articles and our program will use NLP and will find out the similarity index of those articles. It will also tell how much similar these two documents are in percentage. 
Literature Review
Artificial intelligence usage can lead to miracles in the field of computing. Computers can accomplish a task without ever being explicitly programmed to. If you take human linguistics for an instance and incorporate it with the AI, you get Natural Language Processing (NLP).  NLP makes it possible for humans to talk to machines. This branch of AI enables computers to understand, interpret, and manipulate human language.  Through the usage of different algorithms, a simple computer can understand not only the structure of the sentence but also meaning of it. In other words, it can automatically perform different tasks by understanding and responding to the human language. As NLP is a sub-branch of Artificial Intelligence, it further has sub-branches, including natural language understanding (NLU), and natural language generation (NLG).
Natural language processing makes it possible for computers to extract keywords and phrases that can help generating a response. Take Google Assistant, Siri, Alexa, for an instance and Cortana too. The AI bot can understand this text: “Hi Alexa, where is the nearest college?” by transforming it into numbers that makes it easy for machines to understand.
This evolution of AI leads to formation of Search Engines and gave a breakthrough in the field of Information Retrieval.
Problem Statement
“Creating a system that gives us the doc-doc similarity report and is able to search for a specific word details in the dataset.”
Methodology
As our project is based on Natural Language Processing (NLP). We have used techniques of NLP through which we can train our machine on our designed models to get the desired results. In the section, we will discuss the Data Set and the techniques of NLP that are used for the training of our system.      

#### Inverted Index:
The first NLP technique that we are using is inverted index. It is a data structure that is very commonly used to process the textual data in NLP. It stores the relationship of words in the document provided. Below is a simple illustration of how inverted index looks like:

Dictionary	Vector of Document ids
Arrow		18	20	33	41	43	…....
Bunny		10	19	32	45	51	…....
Elephant		9	29	31	36	67	…....
…....							
Zero		12	27	30	47	89	…....
Table: Inverted Index Illustration
As we can infer from the above table, this data structure consists of basically two parts: a dictionary which stores the word and the link of the corresponding documents in which there is occurrence of the words. 
Our projects keeps growing the inverted indexes until each of the document has been processed. Furthermore, our program generates a vector after accessing the relevant information. In addition, we have kept a data structure to record the frequencies of the words. Below is the illustration of how the frequencies will be stored:
Words	           Frequency	
Arrow	   	31
bunny	   	19
…	   …	
zebra	   	13

#### Vector–Space Model:
In the final steps, we are building a document vector for each of the processed document. It utilizes our generated inverted index with a helper data structure to do the required processing. It works with the general idea of assigning the weights to the words in a document relative to other documents as well. By the usage of measures like term frequency and inverse document frequency, it computes the weight for each term in a document.
 
#### Doc-Doc Incidence Matrix:
At last, we are showing the similarity between two documents. The vector-space model with the combination of inverted indexes are being used to calculate the similarity between the provided documents. 
We have n x n matrix, in which:
•	Size is storing the similarity of n documents 
•	Diagonal values are storing the similarity of each document to within itself
If the similarity of the diagonal values are not 1, then it indicated an issue within the program itself. Hence, it is also quite useful while debugging our program.
Experimental Setup
We conducted a complete test run on the system:
System Specifications:
•	CPU: Intel i3-9100F 
Quad-Core with Base clock 3.60 GHz (up to 4.20 GHz Turbo Boost)
•	RAM: 16 GB DDR4
3200 MHz (Dual–Channel)
•	GPU: AMD Radeon RX 580 Series 4GB GDDR5 
Engine Clock up to 1411 MHz
### Environment: The Environments which were used for coding were Google Colab and Anaconda3 Jupyter Notebook
### Dataset
The data set we are using is a basically a collection of novel based-datasets. We have different novel-based data in .txt files. A total of 10 files are being used from d1 to d10. In each .txt file there are huge amount of textual data that we are going to process and will make the system through this project. At the end, when system complete its training, any word can be searched and the program will in just a few seconds will provide all the data related to that specific word in the dataset. 
 
The above snapshot is from one of the datasets that gives the idea that what kind of text is given to our program as input.
Libraries Included
From Stemming to Sklearn, we have included a number of libraries to help make our task much simpler and easier:
 
As we can see from above, we have imported OS, Math, RE or Regular Expression, Stemming, Numpy and Sklearn. Among these, Sklearn library is the one which takes all the spotlight here.
Scikit-learn (Sklearn):
 
One of the most important built-in libraries of python. Sklearn is created to perform ML (Machine Learning) tasks. It has multiple built in implementations of clustering, regression, classification, gradient boosting, and it also has cosine similarity – one which we are using in our project. The cosine similarity is being used to detect the similarities between our documents of the dataset. 
Modules
Our designed-program has two modules:
1.	Doc-Doc Similarity:	Basically, instead of building up the cosine similarity indexing code from the scratch, as mentioned earlier, we used a library from the sklearn module of python. It is a machine learning library available for python and we are using it to detect the documents that have the similarity between them. This is exactly what happens in the Plagiarism detection software. A doc-doc incidence matrix is formed and according to this, the results are visualized that how much work of each students is plagiarized. 
We have the following functionalities in this module:
•	Tokenizing
•	Stemming
•	Removing Stop Words
•	Computing Weights
•	Assigning Term and Document ids
•	Cosine Similarity

2.	Search Engine: The second module is of the Search Engine. The documents are made already in the previous module, so this module basically searches for a specific in the made documents list. Working on the dictionary, we have the term ids stored in it and by getting a key i.e. the word required to be searched, we can look for the details of the word in the dataset. 
 
### Data Pre-Processing
Before we feed Data into our system, the RAW data must be pre-processed. Therefore we, just like any other NLP project, has applied these three basic techniques to pre-process the data before we move a step ahead.
•	Stemming
•	Tokenization
•	Removal of Stop Words
### Results
The total dataset test time performed on the complete dataset topped up to 16 hours of execution. In our execution we calculated the doc-doc incidence matrix and the results achieved were as follows:  
Conclusion
This project was need of the hours. As most of our academic work is shifted to online so there was a need for a system which can check for the percentage of similarity between two or more documents. Because plagiarism is a huge issue till date and as there is more and more work so it is very difficult for the instructor to check for plagiarism. So in this project we solved the same problem and we used the concepts of artificial intelligence like NLP and similarity index processing to find the percentage of similarity between the documents. Also to make this system more complete we added a new functionality through which we can find the exact occurrence of a word in the documents. And we used vector space functionality to solve this problem.  
