# ShortAnswerScoring

This project makes use of the sentence similarity LSTM model (Proj_Sentence_Similarity) to assign a grade to a student answer given a teacher's expected answer in the form of a short paragraph of a few sentences.

Scoring is based on pooling and agregating all possible combinations of pair-wise sentence similarities between the 2 answers. 

    Scoring formula :
    1. For each sentence in first text (Text1_Sent_i), 
       take the maximum similarity scores with every sentence
       in second text (Text2_Sent_1, Text2_Sent_2 etc) to obtain
       "hits" in student's answer with respect to expected answer content
       in sentence Text1_Sent_i. 

    2. Sum up scores in step 1 and divide by number of sentences in first text

Current model has limitations as described under Sentence_Similarity project.
Further work : 
Proj_Sentence_Similarity LSTM model relies on comparing LSTM-extracted word sequence features extracted and word relationship features from glove word vectors. Results from previous model showed errors tend to fall into too-high-score for low-similarity sentence pairs (x%) and too-low=score for high-similarity sentence pairs (y%).
Using parts of speech tags and dividng sentences into phrases and comparing aligned phrases/parts of speech between sentence pair may further enhance performance.
