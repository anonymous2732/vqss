---
layout: page
---

# Self-Supervised Music Source Separation Using Vector-Quantized Source Category Estimates

**Abstract**  
Music source separation is focused on extracting distinct sonic elements from composite tracks. Historically, many methods have been grounded in supervised learning, necessitating labeled data, which is occasionally constrained in its diversity. More recent methods have delved into N-shot techniques that utilize one or more audio samples to aid in the separation. However, a challenge with some of these methods is the necessity for an audio query during inference, making them less suited for genres with varied timbres and effects. This paper offers a proof-of-concept for a self-supervised music source separation system that eliminates the need for audio queries at inference time. In the training phase, while it adopts a query-based approach, we introduce a modification by substituting the continuous embedding of query audios with a Vector Quantized Variational Autoencoder (VQ-VAE). Trained end-to-end with up to N classes as determined by the VQ-VAE's codebook size, the model seeks to effectively categorize instrument classes. During inference, the input is partitioned into N sources, with some potentially left unutilized based on the mix's instrument makeup. This methodology suggests an alternative avenue for considering source separation across diverse music genres.


## Mel-Spectrograms of Separated Sources

We show mel-spectrograms of example input mixes and separated outputs. For each separation from 0 to 15 the Generator is conditioned on the corresponding quantized embedding. By cross-referencing this visualization with the clustering histogram shown below, it is possible to recognize specific sources.

<img src="spectrograms.png">  

## Source Clustering

We also show the distribution of the different classes of the test set for each quantized embedding found by the system.

<img src="hist.png">  

