<div align="center">

<a href="https://github.com/urumb/flakehound"><img src="assets/hero.svg" width="100%" alt="Noel Jacob Antony. I hunt the tests that lie. On a rainy night a pixel hound in a detective hat follows a row of tests, finds the flaky one and names the cause." /></a>

<code>pip install flakehound</code>&nbsp; · &nbsp;<a href="https://pypi.org/project/flakehound/">PyPI</a>&nbsp; · &nbsp;<a href="mailto:noeljacobantony99@gmail.com">send a tip</a>&nbsp; · &nbsp;<a href="https://buymeacoffee.com/urumb">buy the hound a coffee</a>

</div>

<br />

<img src="assets/h-cases.svg" width="100%" alt="Exhibit A: Closed cases" />

<div align="center">

<a href="https://github.com/urumb/flakehound"><img src="assets/case-flakehound.svg" width="400" alt="flakehound: finds flaky pytest tests and names the cause" /></a>
<a href="https://github.com/urumb/multi-agent-code-auditor"><img src="assets/case-auditor.svg" width="400" alt="Multi-Agent Code Auditor: local-only code audits with static analysis and AI agents" /></a>
<a href="https://urumb.github.io/submission-doctor/"><img src="assets/case-doctor.svg" width="400" alt="Submission Doctor: readiness score and fix list for hackathon repos" /></a>
<a href="https://brandproof-wff4.onrender.com/"><img src="assets/case-brandproof.svg" width="400" alt="BrandProof: brand review where every finding quotes its approved source" /></a>
<a href="https://credishield-lyart.vercel.app"><img src="assets/case-credishield.svg" width="400" alt="CrediShield: transparent loan default risk scoring" /></a>
<a href="https://urumb.github.io/hushroom/"><img src="assets/case-hushroom.svg" width="400" alt="Hushroom: a calm focus room for students" /></a>

<sub>Click a file to open it. Source: <a href="https://github.com/urumb/flakehound">flakehound</a> · <a href="https://github.com/urumb/multi-agent-code-auditor">auditor</a> · <a href="https://github.com/urumb/submission-doctor">doctor</a> · <a href="https://github.com/urumb/brandproof">brandproof</a> (Team Maverick, CodeNova India 2026) · <a href="https://github.com/urumb/loan-risk-platform">credishield</a> · <a href="https://github.com/urumb/hushroom">hushroom</a></sub>

</div>

<br />

<img src="assets/h-prints.svg" width="100%" alt="Exhibit B: Fingerprints elsewhere" />

<a href="https://github.com/search?q=author%3Aurumb+is%3Apr+is%3Amerged&type=pullrequests"><img src="assets/board.svg" width="100%" alt="Evidence board: 8 merged pull requests in 7 other projects" /></a>

<details>
<summary>📂 <b>Open the evidence</b> (links to each merged pull request)</summary>
<br />

| Scene | What I left behind |
| :-- | :-- |
| **GoogleCloudPlatform/k8s-aibom** | [Helm chart prints next-step commands after install](https://github.com/GoogleCloudPlatform/k8s-aibom/pull/406) |
| **Lelu-ai/lelu** | [Fixed response mapping in the TypeScript SDK](https://github.com/Lelu-ai/lelu/pull/130) · [Corrected audit page claims](https://github.com/Lelu-ai/lelu/pull/141) |
| **Avenx-JS/avenx-js** | [Updated router guard docs](https://github.com/Avenx-JS/avenx-js/pull/1777) |
| **lenny-ts/caddy-analyzer** | [Fixed blocklist parsing with trailing comments](https://github.com/lenny-ts/caddy-analyzer/pull/151) |
| **wmentor/go-magnetar** | [Added unit tests for a GitLab tool](https://github.com/wmentor/go-magnetar/pull/385) |
| **GianlucaBave/murmury** | [Added tests for the eval harness](https://github.com/GianlucaBave/murmury/pull/94) |
| **Rohan-Shridhar/gridcraft** | [Added a way back from the 404 page](https://github.com/Rohan-Shridhar/gridcraft/pull/151) |

</details>

<br />

<img src="assets/h-locker.svg" width="100%" alt="Exhibit C: The evidence locker" />

Things confiscated after midnight. All of them are clickable.

- 💨 [**FARTLE**](https://urumb.github.io/fartle/): a daily word ladder that always ends in one place
- ⏪ [**One Second Ago**](https://github.com/urumb/one-second-ago): rewind yourself, but the world doesn't
- 🌍 [**Live Threat Map**](https://urumb.github.io/DDOS-attack-map/): a 3D globe of *simulated* cyber attacks
- ⌨️ [**Typing Test**](https://urumb.github.io/typing-test/): how fast are your fingers?
- 📸 [**Polaroid**](https://urumb.github.io/polaroid/): a little Polaroid experiment
- 🍩 [**Donut Factory**](https://urumb.github.io/donut/): a bakery page with a bitable donut cursor

<br />

<img src="assets/h-cold.svg" width="100%" alt="Exhibit D: The lineup" />

One of these three tests is lying. It can pass on one run and fail on the next. **Pick the culprit.**

<div align="center">

<img src="assets/suspect-1.svg" width="270" alt="Suspect 1: test_total adds 0.5 and 0.25 and expects 0.75" />
<img src="assets/suspect-2.svg" width="270" alt="Suspect 2: test_sorted sorts a set of two letters and compares it to a list" />
<img src="assets/suspect-3.svg" width="270" alt="Suspect 3: test_letters turns a set of two letters into a list and compares it" />

</div>

<details>
<summary>👉 <b>Accuse suspect #1</b></summary>
<br />

❌ **Wrong. Released without charge.** Floats look guilty, but 0.5, 0.25 and 0.75 are all exact in binary. This one passes every time.

</details>

<details>
<summary>👉 <b>Accuse suspect #2</b></summary>
<br />

❌ **Wrong. Solid alibi.** A set has no promised order, but `sorted()` gives it one before the comparison.

</details>

<details>
<summary>👉 <b>Accuse suspect #3</b></summary>
<br />

🚨 **Guilty.** Python randomises string hashing in each new process, so `list(s)` can come out as `['b', 'a']`. Setting `PYTHONHASHSEED` pins the behaviour down.

[**flakehound**](https://github.com/urumb/flakehound) catches this kind of liar for you.

</details>

<br />

**Known associates:** Python, Java, C, C++, JavaScript, TypeScript · Flask, Django, React, Next.js · TensorFlow, PyTorch, scikit-learn, NumPy, Pandas · PostgreSQL, MySQL, SQLite, Prisma

**Currently investigating:** advanced ML, backend system design and real-world deployment

**Open to:** AI/ML projects, open source and student-led tech initiatives

<br />

<a href="mailto:noeljacobantony99@gmail.com"><img src="assets/footer.svg" width="100%" alt="Got a test that lies to you? Send the hound a tip." /></a>
