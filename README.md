# ShortAnswerScoring

This project uses the sentence similarity LSTM model to assign a grade to a student answer given an expected answer comprising of a few sentences

Current model has limitations as described under Sentence_Similarity project.
Further work : 
Current model relie on comparing sentence word sequence features extracted by LSTM and word relationship features from glove word vectors. Results from previous model showed errors tend to fall into too-high-score for low-similarity sentence pairs (x%) and too-low=score for high-similarity sentence pairs (y%).
Using parts of speech tags and dividng sentences into phrases and comparing aligned phrases/parts of speech between sentence pair may further enhance performance.
