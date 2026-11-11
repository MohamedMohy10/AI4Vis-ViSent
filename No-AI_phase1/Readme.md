# Phase I: Investigating Sentiment Classification Behavior

Our project investigates how DistilBERT handles negation and contrastive expressions when performing sentiment analysis.

We used the pretrained DistilBERT sentiment classification model and the validation split of SST-2, containing 872 original movie-review sentences.

First, we evaluated the model on the complete dataset. It achieved **91.06% accuracy**, with 78 misclassified sentences. We then examined whether classification errors were associated with negation and contrastive expressions.

We divided the sentences into four categories:

- Neither negation nor contrast.
- Negation only.
- Contrast only.
- Both negation and contrast.

The results revealed noticeable differences:

| Category | Error rate |
|---|---:|
| Neither | 6.67% |
| Negation only | 14.40% |
| Contrast only | 13.00% |
| Both | 14.89% |

We also performed Fisher's exact tests with Bonferroni correction. The negation-only category showed a statistically significant association with higher classification errors compared with the control group (adjusted p-value: 0.0187). The other two comparisons were not statistically significant after correction.

Finally, we examined individual markers. Negation contractions such as "n't" and contrastive expressions such as "but" showed interesting error patterns.

**Our main conclusion is that sentences containing negation or contrastive markers are associated with higher observed classification error rates. Negation provided the strongest statistical evidence.**

However, our analysis uses keyword-based detection and observational data, so it cannot establish that these expressions directly cause classification errors.





## References and Documentation

These sources where used for implementation.

### Model and Dataset
- [DistilBERT Fine-tuned on SST-2 – Hugging Face](https://huggingface.co/distilbert/distilbert-base-uncased-finetuned-sst-2-english)
- [Stanford Sentiment Treebank (SST-2) – Hugging Face](https://huggingface.co/datasets/stanfordnlp/sst2)

### Model Implementation
- [Hugging Face Transformers – Tokenizer Documentation](https://huggingface.co/docs/transformers/main_classes/tokenizer)
- [Hugging Face Transformers – Auto Classes](https://huggingface.co/docs/transformers/model_doc/auto)
- [Hugging Face Datasets – Loading Datasets](https://huggingface.co/docs/datasets/loading)
- [PyTorch – Inference Mode](https://pytorch.org/docs/stable/generated/torch.inference_mode.html)
- [PyTorch – Softmax](https://pytorch.org/docs/stable/generated/torch.nn.functional.softmax.html)

### Data Analysis and Evaluation
- [Pandas – String Methods](https://pandas.pydata.org/docs/user_guide/text.html)
- [Scikit-learn – Accuracy Score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.accuracy_score.html)
- [Scikit-learn – Classification Report](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.classification_report.html)
- [Scikit-learn – Confusion Matrix](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.confusion_matrix.html)
- [SciPy – Fisher's Exact Test](https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.fisher_exact.html)

### Data Visualization
- [Matplotlib – Pyplot Documentation](https://matplotlib.org/stable/api/pyplot_summary.html)
- [Seaborn – Bar Plot](https://seaborn.pydata.org/generated/seaborn.barplot.html)
- [Seaborn – Box Plot](https://seaborn.pydata.org/generated/seaborn.boxplot.html)
