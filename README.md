# Szymon Jędryczko

I run language-model experiments on one GPU and build offline speech software
for Apple computers.

## Research

[HSPMN](https://github.com/NetBr3ak/HSPMN): Python research code for an unpublished
manuscript on hybrid language models. It compares a learned per-token gate with a
frozen random gate for routing between a Gated DeltaNet recurrent stream and a
Native Sparse Attention stream. I trained models on WikiText-103 at two scales,
140M and 350M (scale names, not exact parameter counts), on one RTX 5090.

A later audit found a bug that shifted the training targets twice, so every
recorded run learned to predict the token two places ahead, not the next token.
The audit also found future-token access in the predictive-coding gate and
automatic NSA block selection, and an incorrect Gated DeltaNet CPU recurrence.
Version 5.1.0 fixes these defects; I have not yet run it at training scale
([reproduction status](https://github.com/NetBr3ak/HSPMN#reproduction-status)).
[Manuscript source (LaTeX)](https://github.com/NetBr3ak/HSPMN/blob/main/paper/HSPMN_v5_draft.tex),
written before the audit.

## Products at Tenzan Logic (closed source)

- [Voxmill](https://tenzanlogic.com/en/): offline transcription for Apple computers.
  Rust, whisper.cpp, Core ML, speaker labels with sherpa-onnx. 7.74% word error
  rate on the 758 read-speech clips of the Polish FLEURS test set (Voxmill Pro,
  Whisper large-v3-turbo Q5_0, normalised text, our measurement, September 2026).
- [Helio](https://tenzanlogic.com/helio/): a demo that analyses solar farms
  from the inverter data they already log.
