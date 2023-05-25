# EgoCOT Dataset: Embodied Chain-of-Thought for vision language pre-training

![Main Figure](https://github.com/EmbodiedGPT/EgoCOT_Dataset/blob/main/assest/egocot_frame.jpg)

## Introduction
Welcome to the official GitHub repository for the EgoCOT Dataset! This dataset is designed to address the challenges in embodied planning by providing a large-scale collection of egocentric videos and corresponding step-by-step planning instructions. We have also extended the dataset to include the EgoVQA dataset, focusing on egocentric human-object interaction video question answering tasks. 

In this README, we will introduce the key features of EgoCOT, its construction process, and the possibilities it offers for various embodied tasks. 

## Key Features
- Large-scale collection: EgoCOT contains a carefully selected set of egocentric videos from the Ego4D dataset [1], ensuring a diverse and extensive range of scenarios for embodied planning.
- Step-by-step language instructions: Each video in \dataset is accompanied by high-quality planning instructions. These instructions have been machine-generated, followed by a semantics-based filtering process, and finally verified by human annotators for accuracy and clarity.
- EgoVQA extension: In addition to EgoCOT, we have created the EgoVQA dataset, which expands on the Ego4D dataset. EgoVQA focuses on egocentric human-object interaction video question answering tasks, providing a broader range of egocentric multi-modal data.

## Construction Process
The construction of EgoCOT involves a meticulous process to ensure the quality and relevance of the data. Here is an overview of the steps involved:

1. Selection of egocentric videos: We carefully curated a subset of egocentric videos from the Ego4D dataset to form the foundation of \dataset. These videos cover a wide range of real-world scenarios and capture diverse embodied experiences.

2. Machine-generated planning instructions: We employed state-of-the-art machine learning techniques to generate initial planning instructions for each video. These instructions serve as a starting point for the subsequent filtering and verification steps.

3. Semantics-based filtering: To enhance the quality of the planning instructions, we applied a semantics-based filtering mechanism. This process helps ensure that the instructions are accurate, meaningful, and aligned with the video content.

4. Human verification: To guarantee the correctness and clarity of the planning instructions, we engaged human annotators to review and verify each instruction. This step helps eliminate any remaining errors or ambiguities, resulting in a reliable dataset.

## EmbodiedGPT: End-to-End Multi-Modal Embodied Foundation Model
EmbodiedGPT is an innovative multi-modal model developed based on the \dataset and EgoVQA datasets. This model provides an end-to-end solution for various embodied tasks, allowing natural and intuitive interaction with the physical world.

Some key tasks that \model can perform include:
- Embodied planning: \model leverages the planning instructions from \dataset to execute chain-of-thought planning tasks efficiently and accurately.
- Embodied VQA: With the EgoVQA dataset, \model is capable of answering questions related to egocentric human-object interaction in videos, enabling a deeper understanding of the embodied environment.
- Embodied control: Through the integration of multi-modal data, \model can effectively control and interact with the physical world, enhancing its embodiment capabilities.


## 🖊️ Citation

If you find this project useful in your research, please consider cite:

```BibTeX
@article{anonymousembodiedgpt,
  author    = {Anonymous},
  title     = {EmbodiedGPT: Vision-Language Pre-Training via Embodied Chain of Thought},
  journal   = {Under Review},
  year      = {2023},
}
```
