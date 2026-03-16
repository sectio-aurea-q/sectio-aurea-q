# sectio-aurea-q

Independent security researcher focused on **post-quantum cryptography vulnerabilities**.

I find weaknesses in the cryptographic systems the world is migrating to — before someone else does.

---

### Research: MEGALODON

A multi-phase research program testing whether post-quantum cryptography is as secure as promised.

| Project | What it does | Key findings |
|---|---|---|
| **[megalodon-p1](https://github.com/sectio-aurea-q/megalodon-p1)** | Timing Oracle on CRYSTALS-Kyber (ML-KEM) | ~1200–1500ns timing leak in `indcpa_enc()`. Cohen's d = 0.63–0.73. Microarchitectural cache-line side channel confirmed via disassembly. |
| **[megalodon-p2](https://github.com/sectio-aurea-q/megalodon-p2)** | Process Memory Secret Scanner for Apple Silicon | 16 apps scanned, 8 vulnerable, 71 findings. Signal Desktop: SQLCipher PRAGMA key found 8× in plaintext RAM. Chrome, Safari, Tor Browser, 1Password all affected. |
| **[megalodon-p3](https://github.com/sectio-aurea-q/megalodon-p3)** | Automated PQ Side-Channel Scanner | 7 attack vectors against ML-KEM implementations. |
| **[megalodon-p4](https://github.com/sectio-aurea-q/megalodon-p4)** | Cryptographic Downgrade Engine | MITM strips PQ cipher suites → server falls back to RSA → RSA factored via Pollard's Rho / Fermat. |
| **[megalodon-p5-](https://github.com/sectio-aurea-q/megalodon-p5-)** | Lattice Cryptanalysis Engine | LLL reduction on ML-KEM reduced parameters. dim 8 in 166µs, dim 20 in 26.9s. |
| **[pq-ghost](https://github.com/sectio-aurea-q/pq-ghost)** | PQ Downgrade Attack Framework | **52 targets. 0 survivors.** Every target vulnerable to TLS 1.2 downgrade. 16 had PQ — all Cloudflare-based, all downgradeable. 3 catastrophic (no TLS 1.3): UN, BlackRock, Mastercard. |
| **[megalodon](https://github.com/sectio-aurea-q/megalodon)** | Enterprise Crypto Risk Platform | 10-module CLI. HTML/JSON/Markdown reports. |
| **[megalodon-deepscan](https://github.com/sectio-aurea-q/megalodon-deepscan)** | Post-Quantum Internet Scorecard | Top 50 sites scanned — 24/50 quantum-ready. |

All tools written in **Rust** (P1 in C).

---

### Responsible Disclosure

Active disclosure window: **March 10 – June 8, 2026**

Vendors notified include Telegram, Signal, Chrome/Chromium, Tor, Apple, and 1Password. I follow responsible disclosure timelines. Findings are published only after vendors have been given adequate time to respond.

---

### Contact

📬 **meg.depth@proton.me** (PGP preferred)

---

<p align="center">
  <sub>No team. No institution. Just math.</sub>
</p>
