#Embedding #NLP 

![# Лекция. Детали Word2Vec. FastText, GloVe. Применения эмбеддингов](https://www.youtube.com/watch?v=RKGi26Yk-5A&ab_channel=DeepLearningSchool)
CBOW
Skip-Gram
[[SVD ]] (Сингулярное разложение)

Реализация

```python
import 
embeddings_trained_lemma = Word2Vec(sentences, 
								    vector_size,   
									min_count, 
						            window,
									workers,              
						            sg).wv
```

- sentences - data for model to train on
- vector_size - embedding vector size
- min_count -  Ignores all words with totalfrequency lower than this. 
- window - Maximum distance between the current and predicted word within a sentence
- workers -  Use these many worker threads to train the mode
- sg - CBOW, sg=1 - Skip-Gram