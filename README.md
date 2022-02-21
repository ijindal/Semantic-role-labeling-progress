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
