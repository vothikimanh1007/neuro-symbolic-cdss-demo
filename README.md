# Multimodal Neuro-Symbolic CDSS - Live Dashboard

This repository hosts an interactive, real-time web dashboard demonstrating a multimodal neuro-symbolic framework for Clinical Decision Support Systems (CDSS). 

Based on the 2026 research paper *"Multimodal Neuro-Symbolic Clinical Decision Support: Non-Euclidean Topological Representations as Real-Time Guardrails for Medical Language Models"*, this demo visualizes how continuous topological data can act as mathematical guardrails against LLM semantic hallucinations.

## ✨ Core Features

* **Automated ECG Stream Simulation:** Mimics a real-world ICU monitor by automatically parsing sequential topological data extracted from the MIT-BIH Arrhythmia Database every 2 seconds.
* **Live Topological Telemetry Chart:** A dual-axis moving line chart that plots incoming **H1 Persistence Entropy** and **Topological Amplitude** in real-time.
* **Real-Time Guardrail Adjudication:** As the system streams data, it instantly evaluates the coordinates against safe mathematical bounds (derived from Takens' delay embedding and Vietoris-Rips filtration). 
* **Dynamic LLM Constraints:** The system automatically shifts between **GREEN** (Safe), **YELLOW** (Warning/Context Added), and **RED** (Halted) statuses, intercepting the clinical LLM narrative before a hallucination can occur.

## 📂 Project Structure

* `index.html`: A self-contained, single-page application. It includes all HTML, CSS, and JavaScript. To ensure zero-dependency configuration and prevent Cross-Origin Resource Sharing (CORS) errors, the data subsets are embedded directly within the script.
* `README.md`: Project documentation and deployment guide.

## 🚀 How to Run the Demo

Because all necessary logic and data are embedded directly into `index.html`, there is no need to set up a backend server, Python environment, or database.

### Local Execution
1. Clone or download this repository to your local machine.
2. Double-click the `index.html` file to open it in any modern web browser (Chrome, Edge, Firefox, Safari).
3. Click the **"▶ START STREAM"** button to initiate the live simulation.

### GitHub Pages Deployment (Live Web Hosting)
To host this live on the web for free using GitHub Pages:
1. Ensure both `index.html` and `README.md` are pushed to the `main` branch of your GitHub repository.
2. In your GitHub repository, navigate to the **Settings** tab.
3. On the left sidebar, click on **Pages**.
4. Under "Build and deployment", set the **Source** to `Deploy from a branch`.
5. Select your `main` branch and click **Save**.
6. GitHub will build the site (this usually takes 1-2 minutes). Once finished, your live interactive demo will be accessible at `https://[your-username].github.io/[repo-name]/`.

## 📊 Embedded Datasets

The dashboard utilizes exact data subsets extracted from the paper's original Topological Data Analysis (TDA) sets:
* **Statistical Boundaries:** Extracted from `tda_statistical_profile.json`, mapping the safe H1 Entropy and Amplitude bounds for normal physiological states.
* **Clinical Data Sequence:** Extracted from `tda_mitdb_clinical_dataset.csv` and `tda_nlp_analysis_results.csv`, simulating an incoming window of patient data including normal sinus rhythms, high-frequency noise, and severe anomalies.
