# Phase I: GenAI Usage Reflection Report

**AI-Aided Pair:**
  - Student A (Sahil Sahil / K12541594)
  - Student B (Name / Student ID) 

## Workflow Velocity & Breadth
Leveraging GenAI significantly sped up setup time for data ingestion, string parsing, and plot rendering. Rather than manually referencing Seaborn documentation or boilerplate pipeline syntax, we bootstrapped the experimental setup immediately. This efficiency allowed us to allocate more time to designing targeted synthetic edge cases (e.g., multi-clause sentences combining negations with contrastive modifiers).

## Verification & Analytical Overhead
While AI assistance reduced coding friction, verifying output correctness remained essential. Inspecting score extraction logic and ensuring chart alignment required manual validation. Relying on AI for visualization setup saved time, but interpreting the results remained a human-driven process.

## Core Model Behavioral Discovery
The visualization pipeline exposed a key behavioral pattern: DistilBERT does not merely fail on negated or contrastive logic; it fails with high confidence. Across incorrect predictions on negated inputs, the model maintained mean confidence scores between 91% and 98%, demonstrating severe overconfidence in its failure modes.
