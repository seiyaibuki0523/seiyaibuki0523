## Casper Chen <sub>· Cappuccinoo</sub>

Security researcher at Cevanex, New Taipei City, Taiwan. I work on software security, large language models, and their application to automated vulnerability detection — in particular on making LLM-based detectors trustworthy by verifying what they report rather than shipping it as found. The same work turns up real bugs in open-source projects, which I report upstream (four CVEs in 2026, listed below).

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

### Vulnerability disclosures

Found with the pipeline described above (the memos pair) or by model-assisted review of its candidate reports (mini-snmpd, uftpd), then reported to the maintainers and fixed upstream. All credits are public.

| CVE | Issue | CVSS 3.1 | Affected → fixed |
|---|---|---|---|
| [CVE-2026-51584](https://www.cve.org/CVERecord?id=CVE-2026-51584)<br>[usememos/memos](https://github.com/usememos/memos) | SSO sign-in trusted an attacker-controllable identifier instead of the IdP subject claim → unauthenticated account takeover (CWE-287) · [write-up](https://gist.github.com/seiyaibuki0523/33a4c06eb7d10914e5e5152ecd5100ec) | **9.8 Critical** | ≤ v0.27.1 → v0.28.0 |
| [CVE-2026-51583](https://www.cve.org/CVERecord?id=CVE-2026-51583)<br>[usememos/memos](https://github.com/usememos/memos) | Authenticated SSRF through webhook-target validation, reaching internal addresses (CWE-918) · [write-up](https://gist.github.com/seiyaibuki0523/d8af15eb555808319a2633269a9ebb80) | **8.5 High** | ≤ v0.30.0 |
| [CVE-2026-59961](https://github.com/troglobit/mini-snmpd/security/advisories/GHSA-c9g2-5ghh-8g8c)<br>[troglobit/mini-snmpd](https://github.com/troglobit/mini-snmpd) | Unauthenticated out-of-bounds read in the SNMP request parser; one crafted UDP packet crashes the daemon before the community string is checked (CWE-125) | **8.2 High** | ≤ 1.6 → 1.7 |
| [CVE-2026-59964](https://github.com/troglobit/uftpd/security/advisories/GHSA-vqhc-mmjf-972h)<br>[troglobit/uftpd](https://github.com/troglobit/uftpd) | Stack-based buffer overflow in `compose_path()` via an overlong FTP path from a logged-in or anonymous client (CWE-121) | **5.9 Medium** | ≤ 2.15 → 2.16 |

### Contact

casperchen@cappuccinoo.com · [ORCID 0009-0002-8175-4236](https://orcid.org/0009-0002-8175-4236)

[![GitHub followers](https://img.shields.io/github/followers/seiyaibuki0523?style=flat&logo=github&logoColor=white&label=followers&color=181717)](https://github.com/seiyaibuki0523?tab=followers)
[![GitHub stars](https://img.shields.io/github/stars/seiyaibuki0523?affiliations=OWNER&style=flat&logo=github&logoColor=white&label=stars&color=181717)](https://github.com/seiyaibuki0523?tab=repositories)
