# Transformer Training 07 — Stability: Loss Spikes and Their Cures

Large runs fail in two ways small ones rarely show: the loss jumps, or part of the model quietly saturates. Both reproduced on a tiny model: attention-logit growth and QK-norm, z-loss, one bad batch, clipping and skipping, and what large runs report doing.

**Live site:** https://brendanjameslynskey.github.io/Transformer_Training_07_Stability/

Attention-logit growth and entropy collapse; QK-norm and z-loss; one bad batch; gradient clipping and skipping; what large runs report (PaLM restarts, Adam-driven divergence, lower β<sub>2</sub>).

## Live, animated companion

This deck is the slide companion to Part 2 (Training) of [Transformer Decoder Explained](https://transformer-decoder-explained.vercel.app/training), where the same model trains in your browser:

- [Chapter 8: Stability](https://transformer-decoder-explained.vercel.app/training/08-stability)

## Where the numbers come from

Every measured number on these slides comes from the site's [results.md](https://github.com/BrendanJamesLynskey/transformer-explainer/blob/main/results.md) (seeded NumPy reference runs; CI recomputes them), filled in at build time from its `results.json`. Numbers from papers are cited on the slide with a link. The model is tiny (5,376 parameters, one book, a CPU): its runs show mechanisms, not what happens at scale, and the slides say so where it matters. GPU runs of the site's Colab notebooks are pending; no GPU number appears here.

Part of the [Transformer Training sub-hub](https://github.com/BrendanJamesLynskey/LLM_Hub_Transformer_Training) &middot; [LLMs hub](https://github.com/BrendanJamesLynskey/LLMs)
