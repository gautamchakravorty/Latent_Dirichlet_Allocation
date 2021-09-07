# Latent_Dirichlet_Allocation
NLP/Topic Modelling

Note: This is a living document and the content may change over time due to progress made.

***********Outcome*************************************************************************************************************************

Scenario: 
          When a ticket/query is raised by user, near possible matches of previously resolved email documents/tickets will be displayed for reference.
Benefits: 
          Manual analysis efforts can be saved
          Quicker resolution of the ticket
          Repeatable tickets resolved strategically
          No missing emails
          Fungible support teams
          System managed knowledge repository

Benefits to be quantified:  SR (%), INC (%) closure via automation.

Solution Draft:

Data Preparation:
          Pull the historical data dump of the emails to/from production support email id/email box and setup a scheduled service to pull fresh emails.
          Load cleaned email documents into database.
          Map each email document against the service tickets, if possible.

Modelling:

The ML model will be developed to serve below purpose:
          Generate the topics from the document corpus and consolidate similar documents/tickets on the basis of these topics. 
          The new query raised to production support will be assessed against semantic proximity to matching documents/topic/tickets and share advice.
          Automated closure of ticket, if solved through automation


Below are the recommended models evaluated for the purpose:
          Jaccard Similarity ☹☹☹, 
          Different embeddings+ K-means ☹☹, 
          Different embeddings+ Cosine Similarity ☹, 
          Word2Vec + Smooth Inverse Frequency + Cosine Similarity 😊, 
          Different embeddings+LSI + Cosine Similarity ☹, 
          Different embeddings+ LDA + Jensen-Shannon distance 😊, 
          Different embeddings+ Word Mover Distance 😊😊, 
          Different embeddings+ Variational Auto Encoder (VAE) 😊 😊, 
          Different embeddings+ Universal sentence encoder 😊😊, 
          Different embeddings+ Siamese Manhattan LSTM 😊😊😊, 
          BERT embeddings + Cosine Similarity ❤, 
          Knowledge-based Measures ❤ 
          
          Different embeddings are:
          - Bag of Words (BoW)
          - Term Frequency - Inverse Document Frequency (TF-IDF)
          - Continuous BoW (CBOW) model and SkipGram model embedding(SkipGram)
          - Pre-trained word embedding models : 
           -> Word2Vec (by Google)
           -> GloVe (by Stanford)
           -> fastText (by Facebook)
          - Poincarré embedding
          - Node2Vec embedding based on Random Walk and Graph


Next steps:
          Research and select model solution - Done
          Create dummy data set with both similar/dissimilar tickets - In Progress
          Evaluate the model on the data set to mark satisfaction
          Proof of Concept
          Implementation

