---
description: "SLO-aware 5G multi-access edge computing with SMEC"
hide:
  - navigation
  - toc
---

<div align="center">
  <img src="assets/img/smec-logo-horizontal.png" alt="SMEC logo" style="height: 100px; margin: 0px 0 0px" />
  <h1 style="font-size: 1.2rem; margin-bottom: 0px">SLO-Aware Cellular Multi-Access Edge Computing</h1>
</div>


<div align="center" style="max-width: 980px; margin: 0.75rem auto 0; padding: 0 16px">
  <p style="margin: 0; font-size: 1.05rem; line-height: 1.6">
    Practical, SLO-aware resource management for 5G multi-access edge computing
  </p>
</div>

<div align="center" style="max-width: 980px; margin: 1rem auto 1.25rem; padding: 0 16px">
  <!--
  <div style="font-size: 1rem; line-height: 1.35">
    <strong><a href="https://timez-zx.github.io/">Xiao Zhang</a></strong> · <strong><a href="https://daehyeok.kim">Daehyeok Kim</a></strong>
  </div>
  <div style="font-size: 0.92rem; color: #6b7280; line-height: 1.35">
    The University of Texas at Austin
  </div>
  -->
  <div style="display: flex; flex-wrap: wrap; gap: 10px; justify-content: center; margin-top: 0.85rem">
    <a href="https://github.com/smec-project" class="md-button md-button--primary">GitHub (Coming soon!)</a>
    <a href="https://daehyeok.kim/assets/papers/smec-nsdi26.pdf" class="md-button">NSDI'26 Paper (Coming soon!)</a>
  </div>
</div>

<figure markdown>

<div style="max-width: 1100px; margin: 0 auto; border: 2px dashed #9ca3af; border-radius: 12px; padding: 34px 18px; text-align: center; color: #6b7280">
  <div style="font-weight: 700; letter-spacing: 0.02em">[Placeholder]</div>
  <div style="margin-top: 6px">Main system figure will be placed here.</div>
</div>

</figure>

Our core insight is that standard 5G protocols and MEC application behaviors already expose the signals needed for SLO-aware scheduling <strong>without requiring RAN-edge coordination</strong>.
SMEC exploits these readily available signals through three key ideas:

1. **Exploiting 5G control signals for request identification at the RAN**: Standard 5G control signaling between UE and base station naturally exhibits distinctive patterns when new application requests are generated. SMEC leverages them to detect request boundaries at the RAN without payload inspection or protocol modifications.
2. **Leveraging downlink stability for network latency estimation at the edge**: 5G downlink transmissions exhibit more predictable latency than uplink. SMEC exploits this asymmetry through a lightweight probing protocol between edge servers and client devices, enabling accurate latency tracking without RAN-edge coordination.
3. **Utilizing application lifecycle events for processing time prediction at the edge**: MEC applications' request-response behaviors expose key lifecycle events that enable processing time estimation. SMEC tracks these naturally occurring events through server-side APIs and builds execution history, providing sufficient accuracy for deadline-aware scheduling without requiring invasive application changes.


<div class="grid cards" markdown>

-   **Open-source Implementation**

    ---

    **RAN resource manager**: Pluggable scheduling module for srsRAN's MAC layer

    **Edge resource manager**: User-space daemon managing CPU and GPU resources with lightweight client-side timing daemon


-   **Evaluation Highlights**

    ---

    **90–96% SLO satisfaction** across real-world latency-critical applications with SLO requirements ranging from 10s to 100 milliseconds

    **Starvation-free** for best-effort applications sharing remaining bandwidth



</div>

***
## BibTeX

If you find SMEC relevant to your research, please consider citing:

```bibtex
@inproceedings{smec-nsdi26,
  title     = {Enabling SLO-Aware 5G Multi-Access Edge Computing with SMEC},
  author    = {Xiao Zhang and Daehyeok Kim},
  booktitle = {Proceedings of 23rd USENIX Symposium on Networked Systems Design and Implementation {(NSDI)}},
  year      = {2026}
}
```

***
## Contact

Xiao Zhang (zx123@utexas.edu)

Daehyeok Kim (daehyeok@utexas.edu)

***
## Sponsors

<div style="display: flex; align-items: left; justify-content: left; gap: 28px; flex-wrap: wrap; margin-top: 0.75rem">
  <img src="assets/img/ut-logo.png" alt="The University of Texas at Austin" style="height: 128px; width: auto" />
  <img src="assets/img/nsf-logo.png" alt="National Science Foundation" style="height: 128px; width: auto" />
</div>


