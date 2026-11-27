# Szymon Jędryczko

I build AI applications for employees and customers. My work includes hybrid
document search in Qdrant and local model serving with llama.cpp. At Emitel,
I built an assistant that drafts tickets for users to review and confirm
before submission.

[Portfolio in English](https://szymonjedryczko.vercel.app/en) · <a href="https://szymonjedryczko.vercel.app/" lang="pl">Portfolio po polsku</a> · [LinkedIn](https://www.linkedin.com/in/szymon-jedryczko)

## Selected open-source work

| Project | What you can inspect |
|---|---|
| [Astro #18660](https://github.com/withastro/astro/pull/18660) | I reproduced and fixed a variable font preload bug, then added a regression test. The change was merged. |
| [hdfour](https://github.com/NetBr3ak/hdfour) | A read-only HDF4 and HDF-EOS2 reader in Rust, with Python and WebAssembly bindings. Tests compare its output with the reference HDF4 C library. |
| [BETON](https://github.com/NetBr3ak/beton) | Runs installed linters, type checkers and relevant tests after edits in Claude Code. It can follow local Python imports to find affected tests. |

## Outside work

**[Voxmill](https://tenzanlogic.com/en/voxmill/)** transcribes audio offline on Apple
computers. In my September 2026 test, it reached 7.7% word error rate on the
758 Polish read-speech clips in the FLEURS test split, using Whisper
large-v3-turbo Q5_0 and normalised text. I have not measured accuracy on
meetings or interviews. [Method and results](https://tenzanlogic.com/en/voxmill/help/#pliki).

**[HSPMN](https://github.com/NetBr3ak/hspmn)** is an experiment in routing tokens
between Gated DeltaNet and Native Sparse Attention. I withdrew the original
speedup claim. A later audit found an error in the training targets. Version
5.1.0 fixes the reference code, but I have not repeated training at the
original scale.
[Reproduction status](https://github.com/NetBr3ak/hspmn#reproduction-status).
