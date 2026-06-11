# DeeplearningFinalProject

Student name: Seonggu Jeong 22200667


Title: Research for multimodal fusion 


Summary (200 words): Multimodal Machine Translation (MMT) aims to improve translation accuracy by incorporating visual context to resolve linguistic ambiguities. However, practical MMT models frequently suffer from "modality collapse." Because neural networks seek to minimize loss through the path of least resistance, decoders often rely entirely on strong textual priors. Consequently, the model ignores the visual stream, achieving high standard metrics like BLEU while remaining functionally blind to visual context.

To investigate the root causes of this phenomenon, we utilized our Dual Attention Decoder (DAD) baseline. DAD employs a static fusion mechanism, which mathematically incentivizes the decoder to nullify visual weights to avoid noise. To enforce true visual grounding, we proposed three interventions. First, we conducted an architectural search for the optimal cross-modal fusion depth, evaluating bottom-heavy, top-heavy, and hybrid layer configurations. Second, we introduced Text-Guided Attention Pooling to dynamically extract semantically relevant patches from the Vision Transformer (ViT). Third, we implemented an encoder-level InfoNCE auxiliary loss to mathematically synchronize visual and textual representations in the latent space.

Our extensive empirical evaluations on the Multi30k and MSCOCO datasets revealed a striking architectural paradox. Combining top-heavy fusion with InfoNCE alignment optimized linguistic generation, achieving the highest general translation fluency at 41.69 BLEU. However, performance on the CoMMuTE benchmark—a rigorous forced-choice test for visual disambiguation—remained strictly stagnant at approximately 50.00%, representing statistical random chance. This proves that altering fusion depth creates a "depth illusion." Furthermore, providing perfectly aligned visual features is fundamentally insufficient if the decoder's static fusion allows it to safely ignore them. We conclude that modality collapse cannot be solved merely through structural routing or encoder alignment. Future MMT architectures must incorporate dynamic, bias-mitigating mathematical penalties to actively enforce true multimodal dependency.


Presentation youtube link: https://youtu.be/BJ53RC1IbsA
