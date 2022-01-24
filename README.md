# SimDetect - Detection of Similar Questions in a Question Bank

A question can be phrased in numerous ways, which can lead to lots of repitition/redundancy when stored together. This work proposes an unsupervided learning method for detecting questions that may be framed differently, but most certainly elicit the same answer. The project report can be found [here](https://drive.google.com/file/d/1vRiksnDuJFsMYk5eMFX80l2WLM5rHcKX/view?usp=sharing)

Key features of this project:
- Proposed recurrent-DBSCAN, an extension to the original DBSCAN clustering algorithm (refer to the report for details)
- Utilised Word2Vec embeddings for question represetation - Employed weighted aggregation of Word2Vec embeddings of individual words in the question, the weight for each word being the it's TFIDF value
- Additional features include addition of pre-trained language translation and spell check + correction modules to the pipeline to make the model more robust to data and noise

Data is curated from past CBSE class 10 board examination Science (Physics, Chemistry, Biology) and Social Studies (History, Political Science, Georgraphy, Environmental Science) papers. Further, questions from both English and Hindi language test papers were extracted. 

A subset of the output of the model taken from `Latest.ipynb` (Clusters renamed here). To view all the generated clusters, please check `Latest.ipynb`:
```
___________________________________________CLUSTER  A ______________________________________
Differentiate between intensive subsistence farming and commercial farming practiced in India.

State the differences between commercial farming and intensive subsistence farming

Note the similarity and dissimilarity between intensive subsistence farming and commercial farming practiced in India.

Describe any four characteristics of subsistence farming.

Describe the characteristics subsistence farming.

What are the characteristics of subsistence farming.

___________________________________________CLUSTER  B ______________________________________
Mention five functions of political parties performed in a democracy.

What are the functions performed by political parties in a democracy?

Describe any five major functions of political parties performed in a democracy.

Democracy stands much superior to any other form of government in promoting dignity and freedom of the individual. Justify this statement.

Why does democracy stand much superior to any other form of government

What is the role of democracy in promoting dignity and freedom of the individual

Democracies lead to peaceful and harmonious life among citizens. Justify this statement.

State why Democracies lead to peaceful and harmonious life among citizens

How does democracy help in leading peaceful and harmonious life among citizens

When was the Muslim League formed

Explain the objectives of Muslim league

When was the Muslim League formed.Explain the objectives of Muslim league

How does communalism pose a threat to our national unity Explain.

What is the affect of communalism to national unity

Explain with example the affect of communalism to national unity

___________________________________________CLUSTER  C ______________________________________
Explain the term Veto. Name any four countries which have veto power.

What is veto power

What are the countries that have veto power and explain what that is```
