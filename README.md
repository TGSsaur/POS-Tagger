# POS-Tagger
Platform: Google Colab
Implementation:
Trigram and Bigram Model of POS Tagger
Dataset: English Penn Treebank (PTB) corpus
All Tags List: https://www.ling.upenn.edu/courses/Fall_2003/ling001/penn_treebank_pos.html
Overall Accuracy with 36 POS Tags:
Overall accuracy: 82.87272504442674. 

However accuracy was affected due to presence of some unknown tags in Dataset

Class-Wise Accuracy with 36 POS Tags:

Class Wise Accuracy
WRB: 89.74358974358975
FW: 0.0
DT: 98.97652016857315
UH: 0.0
RBR: 4.3478260869565215
NNP: 73.33664349553129
PDT: 0.0
PRP: 91.98813056379822
NN: 87.65625
VBD: 79.11908646003263
WDT: 50.56179775280899
CC: 96.16252821670429
TO: 99.78021978021978
VBN: 66.74418604651163
SYM: 0.0
'': 0.0
PRP$: 96.0
VB: 85.29411764705883
,: 0
NNS: 76.64418212478921
-LRB-: 84.21052631578947
IN: 99.07928388746802
WP$: 0
RB: 69.27966101694916
-RRB-: 100.0
:: 72.09302325581395
MD: 93.54838709677419
NNPS: 31.11111111111111
#: 66.66666666666666
VBG: 42.10526315789473
VBP: 66.80851063829788
WP: 92.72727272727272
CD: 76.10738255033557
RP: 31.25
EX: 50.0
JJR: 70.83333333333334
VBZ: 83.41708542713567
JJ: 67.63925729442971
JJS: 70.45454545454545
LS: 0.0
RBS: 20.0


Overall Accuracy with 4 POS Tags:
Overall accuracy: 90.3793124578712
Where A: All Adverb Tags
      V: Verb Tags
      N: All Noun Tags
      O: Other Tags
Class-Wise Accuracy with 4 POS Tags:
Class Wise Accuracy
A: 69.39999999999999
O: 95.5077086656034
V: 79.27710843373494
N: 90.30146425495262



Change in Accuracy on number of tags collapsing from 36 to 4:
Yes, Accuracy increased on collapsing number of tags from 36 to 4, accuracy increased from 83% to 91%, this increase in accuracy is very good.
According to us accuracy increased because of decrease in number of possibilities of tags for a given word, suppose Tony is a name of person, but it may be name of some other things and both may occur in dataset with different noun tag (Like NN and NNS) so our 36 POS tagging model may classify the word with NN instead of NNS but there is also possibility that NN may be tag for Tony but according to dataset it will be wrong.
But after collapsing 36 Tags to 4 Tags, now Tony will always be tagged as noun ‘N’ irrespective of whether it is NNS or NN. Which will automatically increase transition probability involving N.
Similarly we have many miscellaneous tags in 36 tags set in which all will come in ‘O’ category except Noun, Verb, Adverb which will help the model to properly evaluate the transition probability more accurately.




