---
description: "SLO-aware 5G multi-access edge computing with SMEC"
hide:
  - navigation
  - toc
---

<div align="center">
  <img src="assets/img/smec-logo.png" alt="SMEC logo" style="height: 128px; margin: 8px 0 6px" />
  <h1 style="font-size: 2rem; margin-bottom: 0px">SMEC: SLO-Aware Cellular Multi-Access Edge Computing</h1>
</div>


<div align="center" style="max-width: 980px; margin: 0.75rem auto 0; padding: 0 16px">
  <p style="margin: 0; font-size: 1.05rem; line-height: 1.6">
    Practical, SLO-aware resource management for 5G/6G multi-access edge computing
  </p>
</div>

<div align="center" style="max-width: 980px; margin: 1rem auto 1.25rem; padding: 0 16px">
  <div style="font-size: 1rem; line-height: 1.35">
    <strong>Xiao Zhang</strong> · <strong>Daehyeok Kim</strong>
  </div>
  <div style="font-size: 0.92rem; color: #6b7280; line-height: 1.35">
    The University of Texas at Austin
  </div>
  <div style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center; margin-top: 0.85rem">
    <a href="https://github.com/smec-project" class="md-button md-button--primary">GitHub</a>
    <a href="https://daehyeok.kim/assets/papers/smec-nsdi26.pdf" class="md-button">NSDI'26 Paper</a>
  </div>
</div>

<figure markdown>

<div style="max-width: 1100px; margin: 0 auto; border: 2px dashed #9ca3af; border-radius: 12px; padding: 34px 18px; text-align: center; color: #6b7280">
  <div style="font-weight: 700; letter-spacing: 0.02em">[Placeholder]</div>
  <div style="margin-top: 6px">Main system figure will be placed here.</div>
</div>

</figure>

SMEC’s approach is to make SLOs first-class in MEC scheduling by decomposing end-to-end latency into actionable components and enforcing deadlines without requiring tight RAN–edge coordination.
In particular, SMEC is built around three ideas:

1. **Decouple control while preserving SLO intent**: Split decision-making across the RAN and the edge so each side can act locally, while still aligning to a shared per-request deadline objective.
2. **Use existing signals for deadline awareness**: Derive deadline-relevant state from existing 5G protocol signals and application behaviors, avoiding changes that require new standards or cross-layer interfaces.
3. **Prioritize tail behavior, not averages**: Schedule with explicit attention to high-percentile latency and contention, since tail delay is what drives most SLO violations in practice.


<div class="grid cards" markdown>

-   **Open-source Implementation**

    ---

    **RAN resource manager**: Implemented as a srsRAN's scheduling policy

    **Edge resource manager**: Runs alongside applications on edge servers


-   **SLO improvements for real-world latency-critical applications**

    ---

    **High SLO satisfaction**: **90–96%**

    **Low tail latency**: reduced by up to **122×**, improving performance predictability



</div>

## BibTeX

If your work uses or is inspired by SMEC, please cite our NSDI’26 paper:

```bibtex
@inproceedings{smec-nsdi26,
  title     = {Enabling SLO-Aware 5G Multi-Access Edge Computing with SMEC},
  author    = {Xiao Zhang and Daehyeok Kim},
  booktitle = {Proceedings of 23rd USENIX Symposium on Networked Systems Design and Implementation {(NSDI)}},
  month     = {May},
  year      = {2026}
}
```

## Sponsors

<div style="display: flex; align-items: left; justify-content: left; gap: 28px; flex-wrap: wrap; margin-top: 0.75rem">
  <img src="assets/img/ut-logo.png" alt="The University of Texas at Austin" style="height: 128px; width: auto" />
  <img src="assets/img/nsf-logo.png" alt="National Science Foundation" style="height: 128px; width: auto" />
</div>


