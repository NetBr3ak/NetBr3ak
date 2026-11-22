# Szymon Jędryczko

I build Voxmill, an offline transcription app for Apple computers. I founded
[Tenzan Logic](https://tenzanlogic.com/en/), which makes Voxmill and Helio.

[Personal site (EN)](https://netbr3ak.github.io/) · [Personal site (PL)](https://netbr3ak.github.io/pl/) · [X](https://x.com/NetBr3ak) · [LinkedIn](https://www.linkedin.com/in/szymon-jedryczko)

## Selected open-source projects

| Project | What it does |
|---|---|
| [hdfour](https://github.com/NetBr3ak/hdfour) | A read-only HDF4 and HDF-EOS2 reader in Rust, with Python and WebAssembly bindings. Tests compare its output with the reference HDF4 C library. [Releases](https://github.com/NetBr3ak/hdfour/releases) include Python wheels and a WebAssembly package. |
| [BETON](https://github.com/NetBr3ak/beton) | Runs installed linters, type checkers and relevant tests after edits in Claude Code. For Python, it can follow local imports to find affected tests. [Download a release](https://github.com/NetBr3ak/beton/releases). |

Other projects: [Fruitend](https://netbr3ak.github.io/fruitend/), a CSS illustration with an
element inspector ([Polish version](https://netbr3ak.github.io/fruitend/pl/)) and [Cook Book Chronicles](https://netbr3ak.github.io/Cook-book-Chronicles/),
a recipe site with serving adjustments and cooking timers.

### Contribution to Astro

[withastro/astro #18660](https://github.com/withastro/astro/pull/18660), merged:
preload variable fonts when the requested weight range is inside the file's
range.

## Products at Tenzan Logic (closed source)

- [Voxmill](https://tenzanlogic.com/en/): offline transcription for Apple computers,
  built with Rust, whisper.cpp and Core ML. 7.74% word error rate on the 758
  read-speech clips of the Polish FLEURS test set (Voxmill Pro,
  Whisper large-v3-turbo Q5_0, normalised text, measured by Tenzan Logic,
  September 2026; [method and results](https://tenzanlogic.com/en/voxmill/help/#pliki)).
  Meetings and interviews have not been measured.
- [Helio](https://tenzanlogic.com/helio/en/): a demo that estimates energy lost
  to solar-farm inverter outages and underperformance from the data the inverters
  already log. It uses public data; curtailment orders in the demo are simulated.

## Research

[HSPMN](https://github.com/NetBr3ak/hspmn): Python research code for an unpublished
manuscript on hybrid language models. It compares a learned per-token gate with a
frozen random gate for routing between a Gated DeltaNet recurrent stream and a
Native Sparse Attention stream. I trained models on WikiText-103 at two scales,
140M and 350M (scale names, not exact parameter counts), on one RTX 5090.

A later audit found a bug that shifted the training targets twice, so every
recorded run learned to predict the token two places ahead, not the next token.
The audit also found future-token access in the predictive-coding gate and
automatic NSA block selection, and an incorrect Gated DeltaNet CPU recurrence.
The reference implementation in version 5.1.0 fixes these defects; I have not
yet run it at training scale
([reproduction status](https://github.com/NetBr3ak/hspmn#reproduction-status)).
[Manuscript source (LaTeX)](https://github.com/NetBr3ak/hspmn/blob/main/paper/HSPMN_v5_draft.tex),
written before the audit.
