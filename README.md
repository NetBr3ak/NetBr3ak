# Szymon Jędryczko

I run language-model experiments on one GPU and build offline speech software
for Apple computers.

## Research

[HSPMN](https://github.com/NetBr3ak/HSPMN): hybrid recurrent-attention language
models (Gated DeltaNet with Native Sparse Attention) at 140M and 350M parameters,
trained on one RTX 5090. Unpublished manuscript:
[PDF](https://github.com/NetBr3ak/HSPMN/blob/main/paper/HSPMN_v5_draft.pdf).

A learned per-token gate gave no significant validation-perplexity gain over a
frozen random gate on WikiText-103, at either size (3 seeds per configuration).
The trained gates carried 0.004 to 0.006 bits about the routing label. The
manuscript's bound puts full routing benefit at about 0.72 bits.

## Products at Tenzan Logic (closed source)

- [Voxmill](https://tenzanlogic.com/en/): offline transcription for Apple computers.
  Rust, whisper.cpp, Core ML, speaker labels with sherpa-onnx. 7.74% word error
  rate on the 758 read-speech clips of the Polish FLEURS test set (Voxmill Pro,
  Whisper large-v3-turbo Q5_0, normalised text, our measurement, September 2026).
- [Helio](https://tenzanlogic.com/helio/): a demo that analyses solar farms
  from the inverter data they already log.
