# madlib_pro
from nltk.corpus import wordnet as wn
# this prompts the user with the word verb
verb1 = input("Verb: ")

pos_all = dict()

pos_l = set()
# this section uses wordnet from nltk.corpus to identify the parts of speech for the word that was entered.
for tmp in wn.synsets(verb1):
    if tmp.name().split('.')[0] == verb1:
       pos_l.add(tmp.pos())
       pos_all[verb1] = pos_l

print(pos_all)
# this is checks the dictionary pos_all to see if v is one of the parts of speech for the word the user input
if 'v' in pos_all[verb1]:
    print("verb")
else:
    print("not a verb")
