<div align="center">

[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=26&duration=3200&pause=1000&color=D64545&center=true&vCenter=true&width=820&height=80&lines=Ngoc-Dung+Nguyen;AI+%2F+Machine+Learning+Researcher;Deep+Survival+Analysis+%7C+Cancer+Risk+Prediction;Biomedical+AI+for+Drug+Discovery)](https://ngocdung03.github.io)

<br/>

<a href="https://ngocdung03.github.io"><img src="https://img.shields.io/badge/Portfolio-1F2937?style=for-the-badge&logo=githubpages&logoColor=white" alt="Portfolio"></a>
<a href="mailto:ngocdungnguyen.hmu@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
<a href="https://www.linkedin.com/in/ngoc-dung-nguyen"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
<a href="#-selected-publications"><img src="https://img.shields.io/badge/Publications-5-8B1A1A?style=for-the-badge&logo=googlescholar&logoColor=white" alt="Publications"></a>
<img src="https://img.shields.io/badge/Seoul-South_Korea-4A5568?style=for-the-badge&logo=googlemaps&logoColor=white" alt="Seoul, South Korea">

<br/><br/>

> *Censoring, competing risks, and calibration are not footnotes in medical prediction —*
> *they decide whether a model is useful or misleading.*

</div>

---

<div align="center">

### 🧬 &nbsp; Deep Survival Analysis for Cancer Prevention &nbsp; 🧬
**Peer-reviewed neural-network survival analysis** — *Cancers*, 2023 &nbsp;|&nbsp; **4 years** modelling large prospective cohorts

</div>

---

## ◈ About

I am an **AI/ML researcher** in **Seoul, South Korea**, building deep-learning models that predict cancer risk from large-scale prospective cohort data — end to end, from the data pipeline through training and evaluation.

My path into machine learning came **through medicine rather than around it**. I trained in public health at Hanoi Medical University, then took an MSc at the National Cancer Center Graduate School of Cancer Science & Policy, where I spent two years applying survival analysis to prospective epidemiological cohorts. A later MSc in Financial Engineering added the stochastic-process and quantitative-modelling side.

The combination I care about is a practical one: **deep-learning engineering with a real understanding of the clinical outcome being modelled.** Most of my work is about respecting the statistics of time-to-event data while still using modern architectures.

**Working toward:** applying biomedical AI to **AI-driven drug discovery** — the time-to-event machinery I use for cancer risk transfers directly to preclinical and clinical endpoints, and representation learning for molecules runs on the same tooling.

<br/>

<div align="center">

| Survival & Risk Modelling | Biomedical Data Science |
|:---|:---|
| Deep survival networks — discrete & continuous time | Prospective cohort design & analytic-cohort definition |
| Cox proportional hazards baselines & diagnostics | Censoring, competing risks, informative missingness |
| Calibration over horizon, not just discrimination | Large biomedical dataset integration & cleaning |
| Multi-task risk across cancer types | Reproducible R / Python analysis pipelines |
| Attention mechanisms over patient features | Pre-specified statistical analysis plans |

</div>

---

## ◈ Selected Publications

<table>
<tr><td>

**🏅 A Study on Survival Analysis Methods Using Neural Networks to Prevent Cancers**
*Chulyoung B., Boseon K., Sunha J., Jonghoon L., **Dung NN***
`Cancers` · **2023**
> Neural-network approaches to time-to-event cancer risk, benchmarked against classical survival models.
> **My role:** deep survival modelling · data cleaning · analysis · manuscript

</td></tr>
<tr><td>

**Metabolic health and central obesity are significantly associated with an increased risk of thyroid cancer: Data from the Korean Genome and Epidemiology Study**
***Dung NN**, Jinhee K., Mikyung K.* &nbsp; · &nbsp; 🥇 *first author*
`Cancer Epidemiology, Biomarkers & Prevention` · **2021**
> Cross-classifying metabolic phenotype against central obesity in the KoGES cohort — the risk was not reducible to BMI alone.
> **My role:** research questions · data cleaning · survival analysis · manuscript

</td></tr>
<tr><td>

**A Systematic Review of Effort–Reward Imbalance among Health Workers**
*Huy NV, Mai DL, Thanh NV, **Dung NN**, Anh NT*
`Int. Journal of Health Planning and Management` · **2018**

</td></tr>
<tr><td>

**Patient satisfaction with health-care services at a national institute of ophthalmology**
*Huy NV, **Dung NN**, Hanh LT, Thanh NV* &nbsp; · &nbsp; 🥈 *second author*
`Int. Journal of Health Planning and Management` · **2017**
> **My role:** data collection · logistic-regression analysis · manuscript

</td></tr>
<tr><td>

**Cigarette Smoking among Adolescents aged 13–15 in Viet Nam: Results from GYTS 2014 Data**
*Huong LT, …, **Dung NN**, et al.*
`Asian Pacific Journal of Cancer Prevention` · **2016**
> **My role:** logistic-regression analysis · manuscript

</td></tr>
</table>

**Conference** — *APHA Annual Meeting & Expo*, **2018** · HPV cohort and progression of cervical intraepithelial neoplasia (survival analysis) · **Overseas Academic Conference Scholarship**, National Cancer Center

---

## ◈ Featured Research Code

<table>
<tr>
<td colspan="2">

### 🔬 [nDeep](https://github.com/ngocdung03/nDeep) &nbsp;—&nbsp; Deep Survival Analysis &nbsp;·&nbsp; ⭐ open source
> *Neural network for time-to-event cancer-risk prediction on prospective cohort data*

Cox proportional hazards is interpretable and hard to beat — when the hazard really is proportional and covariate effects are roughly linear. **nDeep replaces the linear predictor with a neural network while keeping the survival machinery intact.**

- Learns a **non-linear risk function** over covariates from prospective cohort data
- Handles **right-censored** observations natively, rather than collapsing the problem into fixed-horizon binary classification
- Produces **individual risk trajectories over time**, not a single scalar score
- Benchmarked against a **Cox PH baseline** on the same cohort and split, so any gain is attributable to the model rather than the preprocessing

`PyTorch` `Survival Analysis` `Cox PH baseline` `Prospective Cohorts` `Python`

</td>
</tr>
</table>

### 🎯 [CanAttend](https://github.com/ngocdung03/CanAttend) — Attention-Based Multi-Task Cancer Risk & Survival
> *PyTorch attention model for multi-task survival analysis across cancer types*

- **Multi-task learning** — predicts risk across **10 cancer types simultaneously**, sharing representation across related outcomes
- **Attention mechanisms** over patient features, surfacing which covariates drive an individual prediction
- Two prediction modes: **cancer development risk** for healthy individuals, and **survival probability** for diagnosed patients
- **Multiple horizons** — 5, 10, and 15-year predictions, evaluated by **Concordance Index**
- Trained on population-level health data

`PyTorch` `Attention` `Multi-Task Learning` `C-Index` `Survival Analysis`

### 📰 [ADnewsHD](https://github.com/ngocdung03/ADnewsHD) — Daily AI/Finance Digest *(side project)*
> *Installable PWA serving one capped daily digest of high-signal AI, finance, and economics news*

A scheduled Python pipeline fetches, filters, summarizes, and ranks items, writing a single `digest.json`; a React PWA reads and renders it. The two halves never call each other at runtime — **that one file is the entire contract**, which keeps each side independently testable.

`Python` `React` `PWA` `LLM Summarization` `Scheduled Pipelines`

---

## ◈ Methods Toolkit

```
Survival Analysis     →  Cox PH · Kaplan-Meier · discrete-time hazards · competing risks
Deep Survival         →  DeepSurv-style risk nets · DeepHit · attention-based multi-task heads
Evaluation            →  Concordance Index · time-dependent AUC · calibration over horizon
                         Brier score · risk-stratified survival curves
Cohort Epidemiology   →  analytic-cohort definition · exposure windows · confounder adjustment
                         proportional-hazards diagnostics · informative-missingness handling
Classical ML          →  logistic regression · regularized GLMs · gradient boosting · feature selection
Architectures         →  Transformers · CNNs · LSTMs / RNNs · multi-task networks
```

---

## ◈ Tech Stack

<div align="center">

**Deep Learning** &nbsp;·&nbsp;
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![Transformers](https://img.shields.io/badge/Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-D00000?style=flat-square&logo=keras&logoColor=white)

**ML & Statistics** &nbsp;·&nbsp;
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square&logo=scipy&logoColor=white)
![lifelines](https://img.shields.io/badge/lifelines-2C7A7B?style=flat-square&logoColor=white)

**Languages** &nbsp;·&nbsp;
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat-square&logo=postgresql&logoColor=white)
![STATA](https://img.shields.io/badge/STATA-1A5F7A?style=flat-square&logoColor=white)

**Platforms & Tooling** &nbsp;·&nbsp;
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)

**Domain** &nbsp;·&nbsp;
![Cancer Epidemiology](https://img.shields.io/badge/Cancer_Epidemiology-8B1A1A?style=flat-square&logoColor=white)
![Biostatistics](https://img.shields.io/badge/Biostatistics-6B46C1?style=flat-square&logoColor=white)
![Clinical Cohorts](https://img.shields.io/badge/Clinical_Cohorts-2C5282?style=flat-square&logoColor=white)
![Medical Prognosis](https://img.shields.io/badge/Medical_Prognosis-2F855A?style=flat-square&logoColor=white)

</div>

---

## ◈ Experience

| | |
|:---|:---|
| **AI Researcher** · MoAdata | *Jan 2022 – present* |
| **Public Health / Data Researcher** · National Cancer Center, South Korea | *May 2020 – Dec 2021* |
| **Researcher** · Vietnam Institute of Applied Medicine | *Jun 2016 – Aug 2017* |
| **Research Assistant** · National COPD Prevention Project, Bach Mai Hospital | *Jan – Jun 2016* |

---

## ◈ Education

**MSc, Financial Engineering** — WorldQuant University, USA · 2021–2024 · *GPA 91/100*

**MSc, Public Health** — NCC Graduate School of Cancer Science & Policy, South Korea · 2017–2019 · *GPA 4.12/4.30*

**BSc, Public Health** — Hanoi Medical University, Vietnam · 2011–2015 · *GPA 7.64/10*

---

## ◈ Credentials & Continuous Learning

<div align="center">

| | |
|:---:|:---|
| 🧠 | **AI VIETNAM — AIO2025**, intensive AI/ML program *(2025)* |
| 🩺 | **AI for Medical Prognosis** — deeplearning.ai |
| ☁️ | **AWS Machine Learning Fundamentals** — Udacity |
| 📈 | **Predictive Analytics Nanodegree** — Udacity |
| 🧮 | **Mathematics for Machine Learning** — Imperial College London |
| 🔬 | **Deep Learning with TensorFlow** — Codecademy |
| 🐳 | **Docker & Kubernetes** · **Advanced Statistical Methods in Python** |
| 📝 | **Good Clinical Practice** · **Writing in the Sciences** — Stanford |

</div>

---

## ◈ Languages

<div align="center">

![English](https://img.shields.io/badge/English-IELTS_7.0-2C5282?style=flat-square)
![Korean](https://img.shields.io/badge/Korean-KIIP_Level_5-8B1A1A?style=flat-square)
![Vietnamese](https://img.shields.io/badge/Vietnamese-Native-2F855A?style=flat-square)

</div>

---

<div align="center">

**Open to research roles in biomedical AI, AI-driven drug discovery, clinical prediction, and deep survival modelling.**

🌐 Full portfolio, publications, and CV → <a href="https://ngocdung03.github.io"><strong>ngocdung03.github.io</strong></a>

<br/>

<a href="mailto:ngocdungnguyen.hmu@gmail.com"><img src="https://img.shields.io/badge/Get_In_Touch-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Get In Touch"></a>

</div>

<!---
ngocdung03/ngocdung03 is a special repository — its README.md renders on the GitHub profile page.
--->
