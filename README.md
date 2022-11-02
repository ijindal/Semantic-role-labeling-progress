# Semantic-role-labeling-progress


Semantic role labeling is a task of identify the predicate-argument structure in a sentence. It basically consists of 4-subtasks
- Identification of Predicate
    + Predicates can be of following types:
        + Verbial
        + Nomial
- Predicate Sense Disambiguation
- Argument identification
    + Arguments can be of two types:
        + Span based
        + Dependency based: where only syntactic head of the argument span is identified.
- Argument classification

### Assumption

Most of the research works in SRL makes the following assumptions:
- Gold: Sentence boundary detection 
- Gold: Sentence tokenized
- Gold: predicate location

In practical scenarios these assumptions does not hold and have a negative impact on the overall performance of a model. 

### Properties

Because of the complexity of the SRL task it is not always immediate to conclude that a particular model is State-of-the-Art. For example: Comparing a SRL model trained on x fine-tuned transformer model with a SRL model trained on y fine-tuned transformer model is not fair. Therefore, in this work we formalize the process of comparing different SRL models based on the following properties: 
- Which dataset is used? CoNLL09, CoNLL05, CoNLL12, FrameNet
- Evaluation Metric: eval05, eval09
- compute predicate
- Computed predicate Sense: yes/NO
- Overall score: yes/no
- Separate score for predicate sense disambiguation?
- Separate score for argument classification?
- Whether syntax information is used in training SRL model?
- Type of Word embeddings used?
    + Fine-tunned embeddings
        * LMs
    + Static embeddings
        * LMs
        * ElMO
        * GLove
        * Seena
        * 
- Type of encoders
    + BiLSTMS
    + BiLSTMS + Attentions
    + NO encoder
- Model ensemble?


### SRL Research

#### Syntax based 

- [LREC 2022] [Syntax-driven Approach for Semantic Role Labeling](http://www.lrec-conf.org/proceedings/lrec2022/pdf/2022.lrec-1.772.pdf) 


#### Syntax agnostic


#### Multilingual


### SRL datasets

#### Gold
- [CoNLL2009]
- [CoNLL2005]
- [CoNLL2012]

#### Silver

- [UP2.0] 

### SRL for downstream applications

#### Machine Translation

- [LREC 2022] [Using Semantic Role Labeling to Improve Neural Machine Translation](http://www.lrec-conf.org/proceedings/lrec2022/pdf/2022.lrec-1.329.pdf)


#### Natural Language Inference

- [NAACL SUKI 2022] [Is Semantic-aware BERT more Linguistically Aware? A Case Study on Natural Language Inference](https://suki-workshop.github.io/assets/paper/3.pdf)
- [Stanford CS224] [Using Semantic Role Labeling to Combat Adversarial SNLI](https://ccrma.stanford.edu/~zhangmf/CS224u/NLU_final_report.pdf)
- [ACL REPL4NLP 2020] [Joint Training with Semantic Role Labeling for Better Generalization in Natural Language Inference](https://aclanthology.org/2020.repl4nlp-1.11.pdf)
- [AAAI 2020] [SemBERT: Semantics-aware BERT for Language Understanding](https://ojs.aaai.org/index.php/AAAI/article/view/6510)


#### Question Answering
- [NAACL SemEval 2022] [Hybrid Question Answering Using Semantic Roles](https://aclanthology.org/2022.semeval-1.178/)


#### Content Moderation and verification
- [ACL FEVER 2022] [A Semantics-Aware Approach to Automated Claim Verification](https://aclanthology.org/2022.fever-1.5/)
- [ACL Constraint 2022] [Are you a hero or a villain? A semantic role labelling approach for detecting harmful memes.](https://aclanthology.org/2022.constraint-1.3/)

#### Populating ontologies
- [Springer AI Law 2021] [Populating legal ontologies using semantic role labeling](https://link.springer.com/article/10.1007/s10506-020-09271-3)
- [2018 ] [Applying semantic role labeling and spreading activation techniques for semantic information retrieval](https://vb.ktu.edu/primo-explore/fulldisplay?docid=ELABAPDB63246995&vid=KTU&lang=en_US)


#### Other applications
- [Proposition Acquisition with SRL] https://github.com/pruizf/pasrl
- [Scientific Reports 2022] [Computing semantic similarity of texts based on deep graph learning with ability to use semantic role label information](https://www.nature.com/articles/s41598-022-19259-5)
- [NAACL 2018] [SRL4ORL: Improving Opinion Role Labeling using Multi-task Learning with Semantic Role Labeling](https://arxiv.org/abs/1711.00768)
- [ Springer AI] [Semantic role labeling for knowledge graph extraction from text](https://link.springer.com/article/10.1007/s13748-021-00241-7)

#### Sentiment Inference
- [KONVENS 2022] [Semantic Role Labeling for Sentiment Inference: A Case Study](https://aclanthology.org/2022.konvens-1.17.pdf)

