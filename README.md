Tensorflow demo using the Large Movie Review Dataset from http://ai.stanford.edu/~amaas/data/sentiment/

All of these models predict sentiment from movie reviews. 


python3, tensorflow-0.8, nltk

To set up:

    1) clone this directory
    2) cd USF/
    3) wget http://ai.stanford.edu/~amaas/data/sentiment/aclImdb_v1.tar.gz
    4) tar -zxvf aclImdb_v1.tar.gz
    5) pip install -R requirements.txt
    6) open the python3 terminal and import nltk
    7) nltk.download()
    8) Enter: d
    9) Enter: punkt
    10) Enter: q
    11) exit python
    12) python3 preprocess.py
    13) cp default_config.py config.py






To run a model:
    python runner.py [command] [-d]

Where command is either:
    tokrnn to run the token (word embedding) RNN 
    charrnn to run the character level rnn
    tokcnn to run a token conv net
    charcnn to run a character conv net
    chartokrnn to run the hierarchical char -> token RNN model

Options -d runs the model in debug mode, which will make all of the size parameters small so the model compiles fast. This is especially important when setting up a large RNN because compiling the graph takes a long time. Run it with -d to make sure that nothing breaks and then stop and run the real model.

This will run on a GPU or CPU.






# Dataset citing:

@InProceedings{maas-EtAl:2011:ACL-HLT2011,
  author    = {Maas, Andrew L.  and  Daly, Raymond E.  and  Pham, Peter T.  and  Huang, Dan  and  Ng, Andrew Y.  and  Potts, Christopher},
  title     = {Learning Word Vectors for Sentiment Analysis},
  booktitle = {Proceedings of the 49th Annual Meeting of the Association for Computational Linguistics: Human Language Technologies},
  month     = {June},
  year      = {2011},
  address   = {Portland, Oregon, USA},
  publisher = {Association for Computational Linguistics},
  pages     = {142--150},
  url       = {http://www.aclweb.org/anthology/P11-1015}
}

References

Potts, Christopher. 2011. On the negativity of negation. In Nan Li and
David Lutz, eds., Proceedings of Semantics and Linguistic Theory 20,
636-659.

Contact

For questions/comments/corrections please contact Andrew Maas
amaas@cs.stanford.edu
