# DeeplearningFinalProject

Student name: Seonggu Jeong 22200667


Title: Research for multimodal fusion 


Summary (200 words): This research explores the structural optimization of Multimodal Machine Translation (MMT) architectures, specifically focusing on finding the ideal placement for text-vision cross-attention layers. We know that integrating visual features extracted via Vision Transformers (ViT) greatly enhances a model's ability to resolve ambiguous words. However, indiscriminately applying this cross-attention mechanism across every single transformer layer creates a massive computational burden.
To solve this efficiency problem, this study evaluates three distinct proposed models—designated as Model A, Model B, and Model C—each representing a different depth of multimodal fusion. Model A tests "Early Fusion" by injecting visual context into encoder layers 1 and 2. Model B examines "Mid Fusion" at layers 3 and 4, while Model C explores "Late Fusion" at layers 5 and 6.
By systematically ablating the cross-attention module's location within the Fairseq framework, the experiment pinpoints the exact stage of linguistic abstraction where visual information provides the greatest benefit. We will evaluate these configurations across two main dimensions: overall translation fluency, measured by standard BLEU scores, and precise visual disambiguation capabilities, rigorously tested through the CoMMuTE framework. Finally, we will compare the convergence rates and parameter efficiency of Models A, B, and C against a heavy, full-fusion baseline. Ultimately, this work provides strong empirical evidence for designing a lightweight, highly efficient MMT architecture without sacrificing robust multimodal alignment.


Presentation youtube link: https://youtu.be/BJ53RC1IbsA
