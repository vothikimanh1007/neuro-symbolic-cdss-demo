# Neuro-Symbolic Clinical Decision Support Dashboard

This repository contains a lightweight, front-end web application demonstrating a multimodal neuro-symbolic framework for Clinical Decision Support Systems (CDSS). 

Based on the research paper *"Multimodal Neuro-Symbolic Clinical Decision Support: Non-Euclidean Topological Representations as Real-Time Guardrails for Medical Language Models"*, this demo visualizes how topological data can act as mathematical guardrails against LLM semantic hallucinations.

## 📂 Project Structure

* `index.html`: The core application. It includes all HTML, CSS, and JavaScript. For maximum reliability and zero dependency configuration, **the research datasets are embedded directly into the JavaScript of this file.**
* `README.md`: This user guide.

## 🚀 How to Run the Code

Because all necessary data is embedded directly into the `index.html` file, there is no need to set up a backend server, Python environment, or database. 

### Local Execution
1. Download or clone this repository.
2. Double-click the `index.html` file to open it in any modern web browser (Chrome, Edge, Firefox, Safari).

### GitHub Pages Deployment (Recommended)
You can host this live on the web for free using GitHub Pages:
1. Ensure both `index.html` and `README.md` are pushed to your `main` branch.
2. In your GitHub repository, click on the **Settings** tab.
3. On the left sidebar, click on **Pages**.
4. Under "Build and deployment", set the **Source** to `Deploy from a branch`.
5. Select your `main` branch and click **Save**.
6. GitHub will take a minute or two to build the site. Once finished, your live demo will be available at `https://[your-username].github.io/[repo-name]/`.

## 📊 Embedded Datasets

To ensure the demo runs smoothly and without CORS (Cross-Origin Resource Sharing) errors, subsets of the original research data have been embedded into the script:
* **Statistical Profile**: Extracted from `tda_statistical_profile.json`, mapping H1 Entropy and Amplitude bounds for Normal Sinus, Noisy Signals, and Arrhythmia.
* **NLP Guardrail Log**: Extracted from `tda_nlp_analysis_results.csv`, showcasing how the Topological Guardrail intercepts outputs and categorizes them into GREEN (Safe), YELLOW (Warning), and RED (Halted) states.
