# Attention_is_all_you_need
Implementation of Attention is all you need Paper [Link](https://doi.org/10.48550/arXiv.1706.03762)

# Transformer Model Architecture

The Transformer model, introduced in the paper "Attention is All You Need," is a neural network architecture that uses self-attention mechanisms to process sequential data efficiently.

## Key Components

### Encoder-Decoder Structure

- **Encoder**: Consists of multiple identical layers, each containing:
  - Multi-Head Self-Attention
  - Feed Forward Neural Network
  - Add & Norm Layers

- **Decoder**: Similar to the encoder but includes an additional layer for masked multi-head attention to prevent positions from attending to subsequent positions.

### Attention Mechanisms

- **Scaled Dot-Product Attention**: Computes attention scores using queries (Q), keys (K), and values (V). The scores are scaled and passed through a softmax function to obtain attention weights.

- **Multi-Head Attention**: Allows the model to focus on different parts of the sequence simultaneously by using multiple attention heads. Each head processes input independently, and their outputs are concatenated and linearly transformed.

### Positional Encoding

Since the Transformer does not inherently understand sequence order, positional encoding is added to input embeddings to provide information about the position of each word in the sequence.

## Model Outputs

The output probabilities are generated after passing through linear and softmax layers, which transform the decoder's output into a probability distribution over the target vocabulary.

---

This architecture enables parallelization and improves performance over traditional RNN-based models, making it highly effective for tasks such as machine translation, text summarization, and more.
<img src="Screenshot 2024-10-21 at 10.09.42 PM.png">
<img src="Screenshot 2024-10-21 at 10.09.50 PM.png">
