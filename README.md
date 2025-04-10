# visition_transformer_on_flower_datasets
## Vision Transformers vs. CNN?
.Input Representation: While CNNs process raw pixel values directly, ViT divides the input image into patches and transforms them into tokens.

.Processing Mechanism: CNNs use convolutional and pooling layers to hierarchically capture features at different spatial scales. 

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

