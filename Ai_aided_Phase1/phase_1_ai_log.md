# Phase I: AI Interaction Record (AI-Aided Pair)

## Scope of AI Assistance
Generative AI was utilized primarily as an accelerator for boilerplate code generation, dataset preprocessing templates, and visualization formatting. Architectural decisions, linguistic feature definitions, and model output validation were handled directly by our pair.

## Prompts & Workflow

### 1. Preprocessing & Feature Engineering
- **Prompt:** "Write a Python function using pandas to tag text rows based on a list of negation keywords (e.g., 'not', 'never') and contrastive connectives ('but', 'however')."
- **AI Suggestion:** Suggested basic string matching over tokenized lists.
- **Action Taken:** Adopted the structure and expanded the keyword dictionary to include contracted forms (e.g., `n't`) and complex contrastive modifiers.

### 2. Visualization & Layout Optimization
- **Prompt:** "Generate a Seaborn grouped bar plot displaying DistilBERT confidence scores across categories, segmented by prediction correctness."
- **AI Suggestion:** Provided standard `sns.barplot` setup code.
- **Action Taken:** Accepted the base layout, but refactored label formatting, axis bounds (`plt.ylim`), and tick rotation (`ha='right'`, `rotation=15`) with `bbox_inches='tight'` to eliminate x-axis label clipping during image export.

### 3. Pipeline Integration
- **Prompt:** "Provide a snippet to batch inference scores from Hugging Face sequence classification pipelines into a structured pandas DataFrame."
- **AI Response:** Generated batch inference loop structure.
- **Action Taken:** Integrated and verified dictionary index parsing against actual model logits to ensure proper confidence extraction for binary classification targets.