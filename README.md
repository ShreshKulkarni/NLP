# NLP
Programs related to core Natural Language Processing
## count_words_for_word_cloud.ipynb
This program reads the input line by line and counts no. of paragraphs, sentences, tokens and word types or distinct words. In addition, it also prints out the frequencies of all word types. This program separates the words as tokens and counts punctuations as separate tokens. Also, it doesn’t separate ‘s if its in the possessive capacity which is beneficial if for any reason there is any associativity we are looking which is affected by such punctuations. E.g. if we want to find how many times “Mary’s dog” has been referred in a text counting this word separately might be helpful.
In the end, the program also outputs the word cloud after removing the standard stop words.

**Assumptions:**
1)	Punctuations are separated if they appear in the beginning or end of a word. So, if a period appears at the end of last word of a sentence it will be treated as a separate token, but if it appears in middle of word e.g. mary.james it will be treated as a single word. This gives an advantage where the file names if present in the text are not broken and are treated as such unless they have underscore in the beginning.
2)	Underscore(_) is treated as an alphanumeric character because python regex treats it such. Hence, it is not separated as a different token and considered part of a word.
3)	Contractions that were listed in the problem description i.e. n’t, ‘ve, can’t, won’t, ‘ll, ‘re and ‘m are the only ones handled here.
4)	‘s is only separated if it appears with singular pronouns listed in the problem description viz. he, she, it, that,there,here. Otherwise it will be treated as part of the word.
