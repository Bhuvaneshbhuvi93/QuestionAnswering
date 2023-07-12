# Question Answering Project

This project demonstrates the usage of the Haystack library for question answering tasks using large language models (LLMs). It uses the FARM (Fast & Robust Model) framework for training and prediction.

# Technologies Used

Haystack Framework

Hugging face model

# Dataset

Squad20

# Model Result

```
from haystack import Pipeline, Document
from haystack.utils import print_answers

p = Pipeline()
p.add_node(component=new_reader, name="Reader", inputs=["Query"])
res = p.run(
    query="who is the captain of CSK", documents=[Document(content=context)]
)
print_answers(res,details="medium")

```
```
Inferencing Samples:   0%|          | 0/1 [00:00<?, ? Batches/s]WARNING:haystack.modeling.model.language_model:'segment_ids' is not None, but DistilBert does not use them. They will be ignored.
Inferencing Samples: 100%|██████████| 1/1 [00:00<00:00, 29.30 Batches/s]'Query: who is the captain of CSK'
'Answers:'
[   {   'answer': 'MS Dhoni',
        'context': 've played, more than any other team.[1] The team has been '
                   'captained by MS Dhoni since inception and is currently '
                   'coached by Stephen Fleming. In Januar',
        'score': 0.5396232008934021}]
```
