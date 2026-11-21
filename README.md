# Hi, I'm Elvir

QA analyst with a Python and ML side, based in Bulgaria. I worked as a Software Quality Assurance Analyst at SEGA and have a Master's in Computer Technologies in Engineering. My thesis project, PredictBot, is a local LLM forecaster. I didn't train the model. I built the calibration and the evaluation around it.

I'm looking for a role in QA and test automation, AI/LLM evaluation, data quality or security. Remote, or on-site in Sofia. Bulgarian (native), English (fluent).

[LinkedIn](https://www.linkedin.com/in/elvir-s-472a9027b) · [Email](mailto:salokgit@gmail.com)

## Featured project

### [PredictBot](https://github.com/Buhuihanguoren/PredictBot), local LLM forecaster

Ask it a yes/no question and it gives back a calibrated probability with its reasoning. It runs on a $300 second-hand gaming PC. No API key, no cloud, and an offline mode that makes zero network calls.

| Held-out results on ForecastBench | Brier score |
|---|---|
| PredictBot, all 1,662 questions | **0.186** |
| PredictBot, 210 prediction-market questions | **0.141** |
| Always guess the base rate | 0.240 |
| Always guess 50% | 0.250 |

Lower is better.

How I evaluated it:

- Leave-one-week-out cross-validation over four ForecastBench weeks. Priors are fitted on three weeks and scored on the fourth, so every score is on questions the calibration never saw. Week-to-week standard deviation: 0.017.
- Raw LLM probabilities are overconfident. Shrinking them toward a measured base rate, with separate priors for each question source, is what brings the Brier score from about 0.25 down to 0.19.
- The prompt and global settings were chosen on a separate tuning set, not on the test weeks.
- Sanity check: on 5-minute crypto markets, where no model can have an edge, every configuration scores 0.25. That's the smoke test that the parsing and scoring code is correct.
- 500 predictions pre-registered with a timestamp before the answers were published.
- pytest suite and GitHub Actions CI on Linux, macOS and Windows, Python 3.10 to 3.12.

Built with Python, llama.cpp and Gradio. The model is Qwen 3.5 4B (Q4_K_XL), which fits in 3.4 GB of VRAM on a GTX 1660 Ti Mobile.

The repo also lists published GPT-4 and Gemini scores. Those come from other datasets, so they are there for context, not as a head-to-head comparison.

## Experience

**Software Quality Assurance Analyst at SEGA**, Sofia (Oct 2024 – May 2025)

- Reviewed technical specifications against requirements, traced discrepancies to their root cause and wrote them up for development and management.
- Wrote Python scripts that automated crash-dump analysis and test reporting, cutting manual investigation time by 40%.
- Built internal tools on the Jira API for defect tracking and test-result reporting.
- Reproduced complex defects from Visual Studio crash dumps and full stack traces, and kept test cases and defect records in SQL-based systems during Agile sprints.

I also worked on an automotive assembly line in 2021, building components to technical documentation and quality requirements.

## Security research

Found a privacy bug in the new sharing API of Nextcloud 35 (CVSS 4.3, medium): anyone holding one public share link could see who else the file was shared with. Reported through Nextcloud's HackerOne program and fixed in Nextcloud 35.0.1.

## Other projects

- **[job-listing-pipeline](https://github.com/Buhuihanguoren/job-listing-pipeline)**: collects job listings from public job-board APIs, removes duplicates, filters them by region and by your own block lists, and ranks the rest. 159 offline tests, CI on Linux and Windows.
- **[Lucky Slots](https://github.com/Buhuihanguoren/interactive-slot-game)**: slot machine in vanilla JavaScript and PixiJS. 5×4 reels at 60 fps, 100 generated paylines, weighted symbol odds and object pooling. Includes a symbol-analyzer page that counts the symbols the reels produce, and a demo video.
- **[Treasure Vault](https://github.com/Buhuihanguoren/treasure-vault-game)**: vault-door puzzle in TypeScript with PIXI.js v8, GSAP and Vite. Generates a random 3-step combination and a new one after every wrong move.
- **[Plane Spotter](https://github.com/Buhuihanguoren/Python-Script-Plane-Spotter)**: finds aircraft within a chosen radius using the OpenSky API, Haversine distance and latitude-corrected bounding boxes.
- **[PowerShell System Monitor](https://github.com/Buhuihanguoren/PowerShell-System-Monitor)**: logs CPU and memory usage to CSV every 5 seconds, validates the samples and reports data quality.

## Tech stack

**QA and testing:** `pytest`, `GitHub Actions`, `Jira`, `Confluence`, `Visual Studio`, `regression testing`, `root-cause analysis`

**Languages:** `Python`, `SQL`, `C++`, `C#`, `JavaScript`, `TypeScript`, `PowerShell`, `Bash`, `HTML/CSS`

**ML and data:** `llama.cpp`, `Hugging Face`, `Gradio`, `pandas`, `numpy`, `scikit-learn`, `matplotlib`

**Web and cloud:** `Flask`, `Vercel`, `Firebase`, `MongoDB`, `PixiJS`, `Vite`, `Linux`

**Networking and security:** `TCP/IP`, `routing and switching`, `Cisco Packet Tracer`, `MITRE ATT&CK`, `OSINT`

## Certifications

- CCNA: Enterprise Networking, Security, and Automation (Cisco Networking Academy, 2025)
- CCNA: Switching, Routing, and Wireless Essentials (Cisco Networking Academy, 2024)
- CCNA: Introduction to Networks (Cisco Networking Academy, 2023)

## Education

- **Master's, Computer Technologies in Engineering**, University of Mining and Geology "St. Ivan Rilski", Sofia (2025–2026). Thesis: PredictBot.
- **Bachelor's, Computer Technologies in Engineering**, same university (2021–2025).

Relevant coursework: `Neural Networks`, `Data Mining`, `Statistical Data Processing`, `Data Processing with Python`, `Critical Data Protection and OSINT Methods`, `Data Structures and Algorithms`, `Software Engineering`, `Database Management Systems`, `Computer Networks and Communications`, `Information Protection and Security`, `Applied Statistics`

## Currently listening

![Spotify](https://spotify-github-profile-ashen5523-three.vercel.app/view?uid=v2kyn2tq6dtav2q5yf4bf9fik)

"Temporarily Unavailable" means I'm asleep.

The card comes from [my Spotify widget](https://github.com/Buhuihanguoren/spotify-github-profile): a Flask API on Vercel with Spotify OAuth and token refresh, Firebase for token storage and a 30-second cache. Based on kittinan's open-source spotify-github-profile.

## Contact

Email: salokgit@gmail.com · [LinkedIn](https://www.linkedin.com/in/elvir-s-472a9027b)
