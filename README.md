# Data Science & AI Research Portfolio

Welcome to the repository hosting my personal research and data science portfolio. This site showcases my academic contributions to Artificial Intelligence, specifically Multi-Agent Reinforcement Learning (MARL), alongside industry applications across causal inference, blockchain analytics, recommender systems, and MLOps.

Live Website: https://anastasioskontogiorgis.github.io/ 

---

## About Me

I am a Data Scientist and AI Researcher specialising in multi-agent reinforcement learning. I combine rigorous academic methodologies and scaled industry application, I have over 7 years of domain experience (marketing, e-commerce, fraud risk) and a PhD from Trinity College Dublin. 

*   **Core Research:** Channel-robust emergent communication, reliability-aware graph attention layers, and noise taxonomies in MARL environments.
*   **Methodological Focus:** Diagnosing dataset biases and building production-grade evaluation protocols.

---

## Featured Projects

The website presents a collection of research initiatives and production-grade ML applications detailed below:

### 1. Doctoral Research & Publications (NoisyGraph Framework)
*   **Description:** Focuses on maintaining coordinated behavior in multi-agent systems when communication channels are noisy or lossy. Developed the `NoisyGraph` framework, which integrates geometry-driven network topology, autoencoder-based message reliability scoring within graph attention layers, and post-training channel calibration. Evaluated on connected autonomous vehicle environments, the architecture successfully sustains coordination as the channel degrades. This work includes two peer-reviewed publications and a comprehensive survey under review at JAAMAS.
*   **Tech Stack:** MARL with emergent communication, Graph-Attention Networks, Autoencoders, Simulation.

### 2. UAV Emergent-Communication Swarm (Ongoing Research Continuation)
*   **Description:** Adapting the doctoral `NoisyGraph` framework to mobile topologies. It evaluates how a channel-robust emergent-communication architecture handles unknown area coverage under lossy, unreliable link conditions using staged reward curriculums.
*   **Tech Stack:** PyTorch, Multi-Agent RL, Graph Attention Networks, Emergent Communication.

### 3. Semantic Book Recommender
*   **Description:** An end-to-end redesign replacing traditional lexical matching (TF-IDF) with dense vectors. Fixed a critical historical pandas alignment issue to build a pipeline enriching 15k records with a 2.3x retrieval relevance boost over baseline.
*   **Tech Stack:** Python, Sentence-Transformers, FAISS, Gradio, Open Library API.

### 4. Campaign Uplift & Causal Inference
*   **Description:** Isolates true marketing campaign impact from baseline market trends. Utilizes structural time-series models to construct synthetic controls, exposing treatment selection bias through rigorous placebo testing.
*   **Tech Stack:** Python, statsmodels, CausalImpact, LightGBM, Causal Inference.

### 5. Ethereum Fraud & Data Forensic Analytics
*   **Description:** A deep dive into address behavior on the Ethereum blockchain. Applied non-parametric hypothesis testing and multivariable regressions to diagnose prominent label-leakage artifacts driving 77% of target labels on benchmark sets.
*   **Tech Stack:** R, Python, Quarto, Statistical Inference, Logistic Regression.

### 6. Production Phishing Detection Service
*   **Description:** A containerised FastAPI service outputting calibrated probabilities for flexible risk thresholding. Built with strict data deduplication controls to eliminate historical provenance bias and counter drift.
*   **Tech Stack:** scikit-learn, FastAPI, Docker, Model Calibration, Monitoring.

---

## Architecture & Tech Stack

The front-facing portfolio is optimized for speed, semantic clarity, and clean navigation:
*   **Frontend:** Semantic HTML5, custom CSS3 layout typography, and responsive grid layouts.
*   **Research Notebooks/Reports:** Integrated compilation output via Quarto.
*   **Hosting:** Deployed natively via GitHub Pages.

---

## Local Development

If you want to clone this repository to inspect the structure or run the static components locally:

1. **Clone the repository:**
   ```bash
  	git clone https://github.com/anastasioskontogiorgis/anastasioskontogiorgis.github.io.git
       cd anastasioskontogiorgis.github.io
   ```

2. **Run a local static server:**
   You can view the portfolio by opening `index.html` directly in your browser, or spin up a local server using Python:
   ```bash
   python3 -m http.server 8000
   ```
   Then open `http://localhost:8000` in your web browser.

---

## Repository Structure

```text
├── assets/             # Images, diagrams, figures, and downloadable CV
├── index.html          # Main landing page
├── research.html       # Doctoral research, publications, and papers
├── uav.html            # UAV Swarm project deep-dive
├── book.html           # Semantic Recommender project deep-dive
├── campaign.html       # Causal Inference project deep-dive
├── phishing.html       # Production Phishing service deep-dive
├── styles.css          # Core styling rules and responsive layouts
└── README.md           # This file
```

---

## Contact & Links

*   **GitHub:** [@anastasioskontogiorgis](https://github.com/anastasioskontogiorgis)
*   **LinkedIn:** www.linkedin.com/in/anastasios-kontogiorgis
*   **ORCID:** https://orcid.org/0000-0003-4921-3835
