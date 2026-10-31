## Casper Chen <sub>· Cappuccinoo</sub>

Security researcher at Cevanex, New Taipei City, Taiwan. I work on software security, large language models, and their application to automated vulnerability detection — in particular on making LLM-based detectors trustworthy by verifying what they report rather than shipping it as found.

[![ORCID](https://img.shields.io/badge/ORCID-0009--0002--8175--4236-A6CE39?logo=orcid&logoColor=white)](https://orcid.org/0009-0002-8175-4236)
[![IEEE Access](https://img.shields.io/badge/IEEE%20Access-10.1109%2FACCESS.2026.3739345-00629B?logo=ieee&logoColor=white)](https://doi.org/10.1109/ACCESS.2026.3739345)
[![Zenodo](https://img.shields.io/badge/Zenodo-10.5281%2Fzenodo.22704663-1682D4)](https://doi.org/10.5281/zenodo.22704663)
[![Replication package](https://img.shields.io/badge/GitHub-msfv--replication-181717?logo=github&logoColor=white)](https://github.com/seiyaibuki0523/msfv-replication)

### Publication

**Reducing Hallucinated False Positives in LLM-Based Vulnerability Detection via Multi-Signal Focused Verification**<br>
Casper Chen · *IEEE Access*, vol. 14, pp. 153128–153147, 2026 · published 2 October 2026 · open access (CC BY 4.0)<br>
[Paper on IEEE Xplore](https://ieeexplore.ieee.org/document/11719504) · [doi:10.1109/ACCESS.2026.3739345](https://doi.org/10.1109/ACCESS.2026.3739345) · [Replication package](https://github.com/seiyaibuki0523/msfv-replication) · [Archived package on Zenodo](https://doi.org/10.5281/zenodo.22704663)

LLM-based vulnerability detectors hallucinate, and the resulting false positives bury the genuine findings. The article adds a *multi-signal focused verification* stage after detection: each candidate is weighed against four independent signals — identity, source code, concern, and a proof-of-concept verdict admitted in three states, so that a PoC that fails to compile is withheld rather than counted as counter-evidence. Across four benchmarks in three languages and five independent full-pipeline runs, the stage removes 54.6–64.6 % of shipped findings in the main setting (33.7–75.8 % at the precision-first operating point), reduces shipped findings in all 36 detector–verifier–benchmark configurations, and makes the choice of verifier an explicit precision–recall trade-off.

<details>
<summary>BibTeX</summary>

```bibtex
@article{chen2026msfv,
  author  = {Chen, Casper},
  title   = {Reducing Hallucinated False Positives in {LLM}-Based Vulnerability
             Detection via Multi-Signal Focused Verification},
  journal = {IEEE Access},
  volume  = {14},
  pages   = {153128--153147},
  year    = {2026},
  doi     = {10.1109/ACCESS.2026.3739345}
}
```

</details>

### Replication package — [`msfv-replication`](https://github.com/seiyaibuki0523/msfv-replication)

Everything needed to recompute every table of the article, audit the adjudication study, and re-run the pipeline. The code and documents are on GitHub, byte-identical to the Zenodo archive (verifiable against `CHECKSUMS.sha256`); the 2.8 GB of raw run outputs stay on Zenodo and are fetched and verified by one script.

| Directory | Contents |
|---|---|
| `frozen-code/` | the pipeline exactly as it ran: detection layers 0–5, the multi-signal verification stage, PoC generator / validator / sandbox, Semgrep rule packs |
| `experiments/` | the launcher of every run and the labelled ground truth of the four benchmarks |
| `data/ablation/` | 132 run directories, 964 configurations — the raw output behind every reported number (`scripts/fetch_zenodo_data.sh`) |
| `data/adjudication/` | the 253-item adjudication study: protocol, items, both judges' labels and justifications |
| `analysis/` | `make_tables.sh` regenerates every table from the recorded outputs; the expected output is included |

Versions: Zenodo [v1.0](https://doi.org/10.5281/zenodo.22704663) (complete archive) · [v1.1](https://doi.org/10.5281/zenodo.23030516) (addendum for the accepted article) · git tags `zenodo-v1.0`, `zenodo-v1.1`.

### Contact

casperchen@cappuccinoo.com · [ORCID 0009-0002-8175-4236](https://orcid.org/0009-0002-8175-4236)

<p>
  <a href="https://github.com/anuraghazra/github-readme-stats"><img height="150" src="https://github-readme-stats.vercel.app/api?username=seiyaibuki0523&show_icons=true&bg_color=00000000" alt="GitHub stats" /></a>
  <a href="https://github.com/anuraghazra/github-readme-stats"><img height="150" src="https://github-readme-stats.vercel.app/api/top-langs/?username=seiyaibuki0523&layout=compact&card_width=300" alt="Top languages" /></a>
</p>
