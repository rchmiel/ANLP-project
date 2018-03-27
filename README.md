# ANLP-project
Universität Potsdam - Cognitive Systems - Advanced Natural Language Processing - Final project

It is possible to run the text generation with provided data. We pre-ran all the code and saved all the cleaned data and important lists as files.
To generate sentences run the code in text_generation_model.ipynb. Please make sure to have all used third-party modules properly installed and imported.

source code:
- topic_miner.ipynb	 			                      - starts a miner using tweepy which listens to Twitter and saves streams in .json file
- clean_and_split_topic_corpus.ipynb		        - reads a .json file with Twitter data, cleans it and writes cleaned data into a file
- clean_and_split_trump_corpus.ipynb 		        - takes a raw Trump tweet file, cleans it, splits it into sentences and saves the output                                                   as final Trump corpus which will be used for sentence generation
- tagger.ipynb 					                        - uses the Stanford tagger to tag given sentences and creates a file with word, tag                                                       tuples. Additionaly @ tuples are merged after creating the tagged file, creating a                                                       file with a list of lists containing the tuples
- create_emission_probabilty_dictionary.ipynb 	- calculates the emission probabilities from the tagged topic corpus and stores them in                                                   a file
- find_trump_style_words.ipynb 			            - finds the Trump style words

- text_generation_model.ipynb 			            - this is the main code which generates new Trump style sentences by using the tagged                                                     Trump corpus, the tagged topic corpus and the emission dict

data:
- trump_corpus_14012018.txt 			        - contains all tweets Trump tweeted stored as list of dictionaries from the first one to                                                   14.01.2018
- final_trump_corpus.txt 			            - contains the cleaned Trump sentences line separated
- stanford_tagged_trump_corpus.txt 		    - contains the cleaned and tagged Trump sentences stored as lists with tuple pairs of word and                                             tag
- twitter_stream_example.json			        - contains a sample set of the streamed Twitter data
- twitter_stream_example_edited.json		  - contains a sample set of the edited streamed Twitter data for ijson
- twitter_stream_example_edited.json.txt	- contains a sample set of the cleaned topic sentences line separated
- example_topic_corpus_edited.txt		      - contains a sample set of the cleaned topic sentences line separated
- example_tagged_topic_corpus.txt		      - contains a sample set of the cleaned and tagged topic sentences stored as lists with tuple                                               pairs of word and tag
- stanford_tagged_topic_corpus.txt 		    - contains the cleaned and tagged topic sentences stored as lists with tuple pairs of word and                                             tag
- emission_dict.txt 				              - contains the emission probabilities of every word stored as dictionary
- wordranking.txt				                  - contains the word rankings for sentence generation
- style_dict.txt                          - contains words that occur frequently in a certain context

evaluation:
- evaluation_corpora.pdf		- contains the evaluation of the tagger and the corpora
- evaluation_output.pdf			- contains the evaluation of the output

stanford-parser-python-r22186:
- contains the python interface to the Stanford Parser from 'https://github.com/ayushjaiswal/multipass4coreference/tree/master/stanford-parser-python-r22186'
