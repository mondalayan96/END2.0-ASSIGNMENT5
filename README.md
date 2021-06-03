# END2.0-ASSIGNMENT5

# END2_Assignment_5

# Data Augmentation
Data Augmentation is the process that enables us to increase the size of the training data without actually collecting the data.

![Data Augmentation](https://github.com/Aditya701/END2_Assignment_5/blob/main/Images/augmentation.png?raw=true)
# Different Approaches for Text Data Augmentation

- Back Translation
- Synonym Replacement
- Random Swap
- Random Deletion

## Back Translation

In this method, we translate the text data to some language and then translate it back to the original language. This can help to generate textual data with different words while preserving the context of the text data. 
Language translations APIs like google translate, Bing, Yandex are used to perform the translation. For example, given the sentence:

![Back Translation](https://github.com/Aditya701/END2_Assignment_5/blob/main/Images/back_translation.png?raw=true)
## Synonym Replacement

Randomly choose n words from the sentence that are not stop words. Replace each of these words with one of its synonyms chosen at random. 
For example, given the sentence:
This article will focus on summarizing data augmentation techniques in NLP.
The method randomly selects n words (say two), the words article and techniques, and replaces them with write-up and methods respectively.
This write-up will focus on summarizing data augmentation methods in NLP.
## Random Swap

Randomly choose two words in the sentence and swap their positions. Do this n times. 
For example, given the sentence
This article will focus on summarizing data augmentation techniques in NLP.
The method randomly selects n words (say two), the words article and techniques and swaps them to create a new sentence.
This techniques will focus on summarizing data augmentation article in NLP.
In this method, we translate the text data to some language and then translate it back to the original language. This can help to generate textual data with different words while preserving the context of the text data. 
## Random Deletion

Randomly remove each word in the sentence with probability p. 
For example, given the sentence
This article will focus on summarizing data augmentation techniques in NLP.
The method selects n words (say two), the words will and techniques, and removes them from the sentence.
This article focus on summarizing data augmentation in NLP.
You can go to this repository if you want to apply these techniques to your projects.


# Hyperparameters
- lr = 1e-4
- batch_size = 16
- embedding_dim = 512
- dropout_keep_prob = 0.5
- seed = 42
- output_dim = 5
- hidden_dim1 = 256
- hidden_dim2 = 128
- n_layers = 2  # LSTM layers
- bidirectional = True 

# Model Architect
Bidirectional LSTMs are an extension of traditional LSTMs that can improve model performance on sequence classification problems. In problems where all timesteps of the input sequence are available, Bidirectional LSTMs train two instead of one LSTMs on the input sequence.We have used model parameter bidirectional as True.

model = LSTM(size_of_vocab, embedding_dim, hidden_dim1, hidden_dim2, output_dim, n_layers, bidirectional, dropout_keep_prob)

# Training logs

Train Loss: 1.540 | Train Acc: 33.60%
	 Val. Loss: 1.530 |  Val. Acc: 35.52% 

	Train Loss: 1.415 | Train Acc: 47.84%
	 Val. Loss: 1.502 |  Val. Acc: 37.23% 

	Train Loss: 1.318 | Train Acc: 58.44%
	 Val. Loss: 1.511 |  Val. Acc: 37.77% 

	Train Loss: 1.236 | Train Acc: 66.92%
	 Val. Loss: 1.512 |  Val. Acc: 37.50% 

	Train Loss: 1.178 | Train Acc: 72.79%
	 Val. Loss: 1.513 |  Val. Acc: 37.68% 

	Train Loss: 1.130 | Train Acc: 77.64%
	 Val. Loss: 1.518 |  Val. Acc: 37.10% 

	Train Loss: 1.102 | Train Acc: 80.35%
	 Val. Loss: 1.509 |  Val. Acc: 38.22% 

	Train Loss: 1.078 | Train Acc: 82.71%
	 Val. Loss: 1.526 |  Val. Acc: 36.87% 

	Train Loss: 1.061 | Train Acc: 84.51%
	 Val. Loss: 1.522 |  Val. Acc: 37.05% 

	Train Loss: 1.048 | Train Acc: 85.68%
	 Val. Loss: 1.520 |  Val. Acc: 37.41% 


# Future improvements 
We have plans to apply more augmentation strategies, robust hyperpaprameters tuning to imporve validation accuracy
