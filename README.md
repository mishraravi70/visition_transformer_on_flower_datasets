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

