# 7th DubsTech Datathon 🎉

The DubsTech Datathon is the University of Washington’s first homegrown data science hackathon, bringing together curious minds, creative problem-solvers, and data enthusiasts from across campus and beyond. More details can be viewed [**here**](https://www.notion.so/dubstech-datathon/Welcome-to-the-7th-DubsTech-Datathon-2f546885930c802f9bb7e6eff71b2354).

## Introduction 💻
Hello judges, industry experts, and fellow data enthusiasts! My name is Jah Chen. I am from team **Solo Silo 🚀**. As the name suggests, I am soloing this competition all by my lonesome to test my limit on how much I can accomplish as a data scientist in this tight 24-hour window. 

The prompt I am be tackling in this competition is [**Access to Technology**](https://www.notion.so/dubstech-datathon/Access-to-Technology-2fd46885930c80509110dccef10a94bd) with the dataset I am using sourced from [**AccessGuru**](https://b2find.eudat.eu/dataset/e0aa764f-959c-51a9-9f39-60ac02bbb1c7).

## Prompts 🎯
**Which domains (health, education, government, etc.) have the highest number of accessibility violations?**

**What violation types are most common across domains?**

**Which web domain has the most severe accessibility issues?**

**How can we cluster websites based on similarity in violation patterns to identify “high-risk” domains?**

## Exploration Guide 📊
This repository uses `uv` package manager to manage dependencies for faster installation, but standard `pip` works as well. Install dependencies by running `pip install -r requirements.txt`.

Everything you need to see lives in the `presentation` folder:
*   `Exploration.pdf`: PDF version of the data exploration notebook.
*   `Exploration.html`: HTML version of the dataexploration notebook.
*   `Learning.pdf`: PDF version of the machine learning notebook.
*   `Learning.html`: HTML version of the machine learning notebook.
*   `Presentation.pptx`: The main slide deck.
*   `Presentation.mp4`: A video walkthrough of the presentation.

Additionally, check out the `data` folder if you want to run the code yourself! Just make sure to run `Exploration.ipynb` before `Learning.ipynb`.

## Limitations 🚧
While this analysis provides valuable insights into web accessibility, there are several limitations to consider:

*   **Data Imputation**: Missing values in categorical fields (e.g., `violation_category`) were imputed using the mode. This assumption simplifies the data preparation but might introduce bias if the missingness is correlated with specific website types.

*   **Scraping Bias**: The study is restricted to websites that were successfully scraped. Domains with strict anti-bot measures or severe technical errors prevented data collection, potentially excluding a subset of "high-risk" or highly secured websites from the findings.

*   **Unsupervised Specificity**: The clustering and risk identification rely on unsupervised machine learning. Without ground-truth labels for "accessibility risk," the defined clusters are interpretative based on engineered features (e.g., violation severity, frequency) rather than external validation.

*   **Aggregation Smoothing**: Aggregating metrics to the domain level (using medians and percentiles) helps identify systemic issues but may obscure isolated yet critical violations on specific low-traffic pages.

## Future Work 🌎
This project highlights the systemic nature of web accessibility violations across major sectors. By moving beyond simple counts to severity-weighted clustering, we can better prioritize remediation efforts where they are most needed.

**Future improvements could include:**
*   **Temporal Analysis**: Tracking violation trends over time to measure the impact of remediation efforts.
*   **Real-time Scoring**: Developing a browser extension that uses the trained cluster models to assess website accessibility risk in real-time.
*   **Broadened Scope**: Expanding the dataset to include more diverse international domains and niche industries.

### Acknowledgments
A huge thank you to **DubsTech** for organizing this Datathon and **AccessGuru** for providing the rich dataset that made this analysis possible.

Built with ❤️ by **Jah Chen** (Team Solo Silo 🚀).

## Judge Evaluation🧑‍⚖️

> **Problem Definition & Approach (0–5): 5**

> **Data Exploration & Analysis Depth (0–5): 5**

> **Technical Quality (Metrics / Models / Visualizations) (0–5): 4.5**

> **Insights & Real-World Impact (0–5): 4.5**

> **Documentation & Clarity of Process (0–5): 5**

**Total Score (out of 25): 24**

**Judge Comments:**

This submission showcases sophisticated technical depth through comprehensive feature engineering (17 features spanning severity metrics, WCAG principles, and HTML element distributions) and thoughtful comparison of multiple clustering approaches with clear justification. The severity-weighted risk scoring formula provides actionable prioritization frameworks that move beyond simple violation counts to systemic pattern identification. The transparent documentation of limitations and well-structured notebooks demonstrate strong statistical maturity and scientific rigor.

