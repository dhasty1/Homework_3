# Homework 3

## Executive Summary

While I was unable to complete the Reranker or RAG notebooks, I have researched them previously and believe I know the pros and cons of each. The Baseline Semantic Search was fun to implement. However, I noticed that the results lack a lot to be desired. They were consistently returning around 25-30% accuracy. This is likely due to the quality of the embeddings. If the embeddings are not capturing the the semantics of the text effectively, the results aren't going to be as accurate. 

When I was trying to repurpose the Colab notebook for my usage, I kept getting errors and would have to implement solutions. One of these errors likely messed with the accuracy of my results. In order to get the embeddings to work, I had to improvise the method in which I was retrieving them. I ended up trimming them to 1000 to match the 1000 passages of data I was passing in. While this likely lessened the accuracy in my results, I could not find another way around it as it kept returning indexing errors. In the future, I'd like to explore other embedding models that are smaller yet still effective.

**Recommendation**

Considering the pros and cons of each model, I would recommend adopting the RAG model. From the research I've done, I believe it has superior performance in retrieving relevant documents. The RAG model's integration of authoritative knowledge bases tends to render more accurate responses to queries because it isn't relying on dated training data. Rather, it's able to leverage the most up-to-date information like research, statistic, news sites, social media feeds, etc. to train the model. 

**Production**

Deploying a RAG model into production has been touted as one of the most cheapest and most efficient ways to get started with LLMs for a business. With the use of online cloud-based platforms like AWS and Azure, among others, it can make deployment a breeze. In addition, you can leverage LangChain and an abundance of online resources to build a RAG/LLM model in minutes.

**RAG/LLM’s**

Unfortunately, I cannot attest to my results using RAG as I did not get that far in the assignment. However, I can speak to how the typical results compare to Semantic Search, BM25 and Reranker. Compared to these other models, RAG leverages LLMs so it has access to a wider array of training data. It also has a contextual understanding of the queries in order to return more accurate results. Its ability to accept augmented training data delivers more accurate results as it isn't as static as the other models. RAG models also excel when it comes to handling ambiguity and variability in user queries.

**Fine Tuning**

I don't blame the boss for having an issue with pretrained models like `nq-distilbert-base-v1` as there are better options out there. I would approach fine-tuning by gathering a dataset that is similar to what I'd be using the model for. That way it will cover the topics and language style my model needs to handle. From there, I would choose a pre-trained model that has been trained on data similar to mine. I would then fine-tune my dataset through the pre-trained model and adjust the parameters to better fit my data. This will help the model learn the specific patterns of my dataset. I would accomplish this through prompt engineering as it helps the model understand and respond to the queries in the context of my data. As with any model training, it is an iterative process. Continuous development leads to the most accurate and efficient model.

## Appendix

i. Table of Baseline Semantic Search Results

![Semantic Search Results](images/Homework%203%20Table.png)