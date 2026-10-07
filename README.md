# From Layers to Hardware

A minimal, animated introduction to inference workflow for senior CS undergraduates. Follow data transfers, compute, and overlap instead of treating model layers as a hardware schedule.

## Open the demo

Download `one-matmul.html` and open it in a modern browser. Everything is in one file; no installation, server, or internet connection is needed.

Use the page buttons at the bottom. Play/pause, replay, and the progress slider control the animations. Space pauses; left/right arrow keys change pages when focus is outside a control.

## Five pages

| Page | Main comparison |
| --- | --- |
| 01 Workflow | Operators, tiled data movement, overlap, memory-bound vs. compute-bound execution |
| 02 Quantization | BF16 vs. INT8 weights: Load 0–3 gets shorter |
| 03 Hardware support | General arithmetic vs. matrix acceleration: Compute 0–3 gets shorter |
| 04 Kernel fusion | Separate vs. fused kernels: intermediate HBM writes and reads disappear |
| 05 Speculative decoding | Batch size 8: fewer target weight loads, more verification compute; compare spare compute with a compute-bound device |

Pages 02–05 use synchronized Before/After views with a shared clock and time scale. Timing is illustrative, not a hardware benchmark. Page 05 uses a scripted greedy decoding example with up to three draft tokens per request; both paths produce the same 64 output tokens. Teaching notes and primary-source links are inside the demo.

The UI is in English. Reduced-motion preferences pause the initial animation.

## License

Copyright 2026 Zaiyang Zhang. Licensed under the [Apache License 2.0](LICENSE).
