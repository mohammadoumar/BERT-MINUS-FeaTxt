# Argument Mining with Modular BERT with Selective Fine-tuning

**Abstract:** In this paper, we present a modular, transfer learning enabled BERT--MINUS-FeaTxt model for Link Identification and Argument Type Classification sub-tasks of Argument Mining in the Persuasive Essays dataset. The BERT--MINUS-FeaTxt model consists of four modules: the first module embeds the essay paragraph text. The other three modules contextualize the argument markers, arguments components and Features as Text, respectively. To enable transfer learning, we introduce the Selective Fine-tuning process which implements two kinds of transfer learning in our BERT--MINUS--FeaTxt model: auto-transfer (transfer learning from a task to itself) and cross-transfer (classical transfer learning from one task to another). Our modular BERT--MINUS--FeaTxt model achieves state-of-the-art results on the Link Identification task and competitive results on the Argument Type Classification task. The synergy between the Features as Text mechanism and transfer learning via the Selective Fine-tuning process significantly improve the performance of the model. Our work reveals the importance and potential of Selective Fine-tuning in modular Large Language Models. Moreover, our work dovetails naturally into the Prompt Engineering paradigm in NLP and AI.

# Model

Our model incorporates contextual and structural features of the argument component to build enriched BERT based representation for argument classification. More details about BERT and other transformer models can be found here: https://github.com/huggingface/transformers

<p align="center">
<img src="model.jpg" width="400" height="300" />
</p>

# Data

We experiment on our model with 3 datasets: 

1) *Persuasive Essays*: https://tudatalib.ulb.tu-darmstadt.de/handle/tudatalib/2422

The contextual and structural features of all three datasets have been pre-computed separately. All three datasets in the PyTorch ready ``.pt`` format are given in the ``/datasets`` folder.

# Tasks

We train our model for two tasks: 

1) BERT fine-tune on the three datasets
2) comparing numerical concatenation versus our structural features as text

More details about BERT fine-tuning can be found here: https://huggingface.co/docs/transformers/training

# Notebooks

The notebooks used for the experiments are given in the ``/notebooks`` folder. More detailed explanation about the usage is provided in the ``README`` file in the folder.

# Requirements

We use the following versions of the packages:

```
torch==1.10
transformers==4.12.5
datasets==1.15.1
tensorboard==2.6.0
```

# Platform

All experiments have been performed on Paperspace's Gradient cloud AI/ML platform: https://gradient.run/
