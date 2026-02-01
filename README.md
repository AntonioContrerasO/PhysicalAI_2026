# PhysicalAI Project

## Approach
During this hackathon, we iterated through several architectural ideas, discarding approaches that were ill-suited for the time constraints. We ultimately selected **Action Chunking with Transformers (ACT)** due to its proven data efficiency and ability to generalize from a limited number of demonstrations.

## Data Collection & Challenges
Our initial experimental design aimed for a baseline of 50 teleoperated demonstrations. However, we encountered hardware calibration drifts and latency issues with the `solo-cli` tool.

As a result, we successfully captured a high-quality (but small) dataset of **20 episodes**. While this is slightly below the recommended threshold for standard ACT convergence, it pushed us to innovate on data augmentation.

![Setup Configuration](images/image-1.jpeg)

## Synthetic Data & Augmentation
To overcome the data scarcity, we engineered a synthetic data pipeline:
1. **Frame-Level Augmentation:** We randomly sampled frames from existing episodes and applied stochastic noise and domain randomization techniques to increase visual diversity.
2. **Generative Video Modification:** We experimented with a video-to-video generative model to radically alter environmental attributes (e.g., lighting, textures, and color shifts) while preserving semantic actions.

## Results & Demo
Despite the low-data regime, the policy demonstrates promising capability.

[![Watch the Demo Video](https://raw.githubusercontent.com/username/repository/branch/assets/thumbnail.png)](assets/Demo-simple.mp4)

## Model & Dataset
| Resource | Link |
| :--- | :--- |
| **Model** | [LaLegumbreArtificial/act-real1](https://huggingface.co/LaLegumbreArtificial/act-real1) |
| **Dataset** | [GuilloCarey/real1](https://huggingface.co/datasets/GuilloCarey/real1) |
