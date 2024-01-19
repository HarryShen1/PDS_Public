# PDS_Public
 
Main tasks focused on creating datasets and picking out highly relevant words to feed to GAILA using Java. 

The datasets were created by scraping articles with high enough word count, which were Wikipedia and WikiHow articles on the object/motion for consistency for all the objects/motions. The articles would be copy and pasted into a text file, in which every instance of punctuation would be removed and every phrase of 4 words would be recorded. The datasets would then be created such that it would only include every instance of 4 words containing the attribute would be recorded as a 4gram. 

From these datasets, we chose highly relevant words based on tf-idf values. The tf-idf value of a word is calculated as the product of its frequency within the datasets of 4grams and its inverse frequency within the entire document. This gives a relative ranking of relevance for all the words.

After giving 15 highly relevant attributes from each base word to the machine to train on, we rehashed the 4grams on same articles to gather more potential high relevance words. However, we looked for 4grams containing the words with high tfidf value, and applied the same tfidf calculation to generate more attributes. 

We also create masks of 4grams using attributes of base words, both relevant and irrelevant, where the attributes would be replaced with an asterisk. We then generate patterns that may be common in containing relevant words for further generation.