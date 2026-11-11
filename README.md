# ViSent
Sentiment Analysis under Contextual Negations &amp; Contrastive Modifiers

Our project investigates how a pretrained sentiment analysis model handles negation words (e.g., "not", "never") and contrastive expressions (e.g., "but", "however") when classifying text as positive or negative.

Dataset: Stanford Sentiment Treebank (SST-2), using its labeled validation split, supplemented with synthetically generated sentences containing negations and contrastive modifiers.
https://huggingface.co/datasets/stanfordnlp/sst2

Model: We will use DistilBERT (distilbert-base-uncased-finetuned-sst-2-english), a pretrained transformer model fine-tuned for binary sentiment classification.
We will analyze its predictions and internal representations to investigate the influence of negation and contrastive sentence structures.

Pretrained model: https://huggingface.co/distilbert/distilbert-base-uncased-finetuned-sst-2-english
