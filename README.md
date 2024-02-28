# EgoCOT: Embodied Chain-of-Thought Dataset for Vision Language Pre-training
[Download Link](https://drive.google.com/drive/folders/1d30x7S5MTz85JuqJcacQpp97T6Z2nbMt?usp=sharing)

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
EmbodiedGPT is an innovative multi-modal model developed based on the EgoCOT and EgoVQA datasets. This model provides an end-to-end solution for various embodied tasks, allowing natural and intuitive interaction with the physical world.

Some key tasks that EmboodiedGPT can perform include:
- Embodied planning: EmboodiedGPT leverages the planning instructions from EgoCOT to execute chain-of-thought planning tasks efficiently and accurately.
- Embodied VQA: With the EgoVQA dataset, EmboodiedGPT is capable of answering questions related to egocentric human-object interaction in videos, enabling a deeper understanding of the embodied environment.
- Embodied control: Through the integration of multi-modal data, EmboodiedGPT can effectively control and interact with the physical world, enhancing its embodiment capabilities.


## Description

This dataset contains examples of video data, where each sample consists of a sequence of eight consecutive frames represented as numpy arrays, along with associated captions and embodied planning information. The dataset is intended for tasks related to video analysis, captioning, and embodied planning research. The goal of this dataset is to provide a resource for evaluating the alignment between video data and embodied planning descriptions.

## Data Format

Each data sample in the dataset is represented in JSON format and has the following fields:

- `image`: The file name of the numpy array file containing the sequence of eight consecutive frames representing the video. These frames can be used to reconstruct the video for analysis.
- `caption`: A brief and simple caption describing the content of the video.
- `planning`: The embodied planning information associated with the video. It contains a series of actions required to achieve a specific goal in the given video context. The actions are represented as a string, and each action is listed with a corresponding step number. The format is as follows:

  ```
  pick up the bag of clothes. Put the bag of clothes on the floor.
  actions:
  1. pick up(bag of clothes)
  2. put on(bag of clothes, floor)
  ```

- `score`: A numeric score indicating the alignment between the video and the embodied planning. The score is calculated based on some metric and measures how well the planning description matches the actual content of the video. Any data samples with a score lower than 0.2 have been removed from the dataset during the data cleaning process.

## Data Sample

Below is an example of a single data sample in the dataset:

```
{
  "image": "EGO_1.npy",
  "caption": "C places the bag of clothes on the floor",
  "planing": "pick up the bag of clothes. Put the bag of clothes on the floor.\nactions:\n1. pick up(bag of clothes)\n2. put on(bag of clothes, floor)",
  "score": 0.268310546875
}
```

## Dataset Usage

This dataset is made available for research purposes only. Researchers and developers can utilize this dataset to evaluate and benchmark algorithms and models related to video analysis, captioning, and embodied planning. However, users are required to cite the source of the dataset appropriately in their publications or works.



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
