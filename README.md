# visition_transformer_on_flower_datasets
## Vision Transformers vs. CNN?
Input Representation: While CNNs process raw pixel values directly, ViT divides the input image into patches and transforms them into tokens.

Processing Mechanism: CNNs use convolutional and pooling layers to hierarchically capture features at different spatial scales. 

ViT employs self-attention mechanisms to consider relationships among all patches.

Global Context: ViT inherently captures global context through self-attention, which helps in recognizing relationships between distant patches. 

CNNs rely on pooling layers for coarse global information.

Data Efficiency: CNNs often require large amounts of labeled data for training, whereas ViT can benefit from pre-training on large datasets and then fine-tuning on specific tasks.



![image](https://github.com/user-attachments/assets/8f8daa9b-6f6a-4681-a835-4b3066522c7c)
https://arxiv.org/abs/2010.11929\\

## 1-Patch Embedding:
The input image is divided into fixed-size square patches. Each patch is then linearly transformed into a vector using a learnable linear projection. This results in a sequence of patch embeddings, which serve as the input tokens for the subsequent layers.
![image](https://github.com/user-attachments/assets/870ce9d2-76a3-4b0b-814b-6351fc7205af)
Filters of the initial linear embedding of RGB values of ViT-L/32 model [https://arxiv.org/abs/2010.11929]\\

## 2- Positional Embedding:
Positional encodings help the model differentiate between different positions in the image and capture spatial relationships. They are usually learned and added to the patch embeddings at the input stage.

## 3- Encoder Layers:
The core of the Vision Transformer consists of multiple encoder layers, each containing two primary sub-layers: multi-head self-attention and feedforward neural networks.

i am adding only 6(depth=6) encoder and 12(heads=12) multi self attentions.

## 4-Multi-Head Self-Attention:
The self-attention mechanism captures the relationships between different patches in the input sequence.

For each patch embedding, self-attention computes a weighted sum of all patch embeddings, where the weights are determined by the relevance of each patch to the current one.

This mechanism allows the model to focus on important patches while considering both local and global contexts.

Multi-head attention employs multiple sets of learnable parameters (attention heads) to capture different types of relationships.

## 5-Feedforward Neural Networks:
After self-attention, the output from each patch’s self-attention mechanism is passed through a feedforward neural network.

## 6-Layer Normalization and Residual Connections:
Both the self-attention mechanism and the feedforward network outputs are followed by layer normalization and residual connections.

Layer normalization helps stabilize and speed up training by normalizing the inputs to each sub-layer.

https://medium.com/@hansahettiarachchi/unveiling-vision-transformers-revolutionizing-computer-vision-beyond-convolution-c410110ef061 \\

## what is i am doing in my projects?

## Vision Transformer (ViT) - PyTorch Implementation

This repository contains a clean and modular implementation of the Vision Transformer (ViT) model using PyTorch. It includes model architecture, training loop, evaluation logic, and tracking of training metrics.

## Features
Patch-based embedding with position encodings

Multi-layer Transformer Encoder

MLP Classification head

GPU support (automatically detects CUDA)

Full training loop with accuracy/loss tracking

Evaluation on validation and training sets

## 🧠 Model Architecture
![image](https://github.com/user-attachments/assets/00452f3f-fba3-49b2-8f3b-289df4a012a8)\\

## 📊 Training Results
Epoch 1, Loss: 32.9126, Train Acc: 60.94%, Val Acc: 60.94%.

Epoch 2, Loss: 26.0115, Train Acc: 68.39%, Val Acc: 68.39%.

Epoch 3, Loss: 24.6965, Train Acc: 67.14%, Val Acc: 67.14%.

Epoch 4, Loss: 22.5034, Train Acc: 77.02%, Val Acc: 77.02%

Epoch 5, Loss: 20.8880, Train Acc: 79.69%, Val Acc: 79.69%

Epoch 6, Loss: 19.0360, Train Acc: 82.12%, Val Acc: 82.12%

Epoch 7, Loss: 15.9342, Train Acc: 90.20%, Val Acc: 90.20%

Epoch 8, Loss: 14.6774, Train Acc: 89.18%, Val Acc: 89.18%

Epoch 9, Loss: 11.5833, Train Acc: 92.31%, Val Acc: 92.31%

Epoch 10, Loss: 9.7569, Train Acc: 94.98%, Val Acc: 94.98%

Epoch 11, Loss: 8.8576, Train Acc: 92.39%, Val Acc: 92.39%

Epoch 12, Loss: 7.3984, Train Acc: 94.67%, Val Acc: 94.67%

Epoch 13, Loss: 5.2256, Train Acc: 97.10%, Val Acc: 97.10%

Epoch 14, Loss: 6.1003, Train Acc: 95.61%, Val Acc: 95.61%

Epoch 15, Loss: 5.6882, Train Acc: 97.25%, Val Acc: 97.25%

Epoch 16, Loss: 6.5714, Train Acc: 96.86%, Val Acc: 96.86%

Epoch 17, Loss: 5.8495, Train Acc: 95.76%, Val Acc: 95.76%

Epoch 18, Loss: 3.9325, Train Acc: 97.25%, Val Acc: 97.25%

Epoch 19, Loss: 3.6671, Train Acc: 97.57%, Val Acc: 97.57%

Epoch 20, Loss: 3.3106, Train Acc: 97.41%, Val Acc: 97.41%

Epoch 21, Loss: 2.5899, Train Acc: 98.98%, Val Acc: 98.98%

Epoch 22, Loss: 2.8149, Train Acc: 99.22%, Val Acc: 99.22%

Epoch 23, Loss: 1.8207, Train Acc: 98.82%, Val Acc: 98.82%

Epoch 24, Loss: 2.0974, Train Acc: 99.45%, Val Acc: 99.45%

Epoch 25, Loss: 2.3796, Train Acc: 98.51%, Val Acc: 98.51%

Epoch 26, Loss: 4.2137, Train Acc: 98.90%, Val Acc: 98.90%

Epoch 27, Loss: 2.9976, Train Acc: 98.75%, Val Acc: 98.75%

Epoch 28, Loss: 4.5717, Train Acc: 93.57%, Val Acc: 93.57%

Epoch 29, Loss: 3.6370, Train Acc: 99.22%, Val Acc: 99.22%

Epoch 30, Loss: 2.6980, Train Acc: 98.04%, Val Acc: 98.04%

## Predictions



