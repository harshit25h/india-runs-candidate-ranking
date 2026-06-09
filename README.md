# India.Runs Candidate Ranking System

## Team Information

**Team Name:** TalentLens AI  
**Team Leader:** Harshit Kumar  
**Challenge:** India.Runs Data & AI Challenge  
**Problem Statement:** AI-Powered Candidate Ranking and Recommendation System

---

# Overview

This project presents an intelligent candidate ranking and recommendation system designed to identify the most suitable candidates for a given job description.

Traditional recruitment systems rely heavily on keyword matching, which often overlooks highly qualified candidates. Our solution combines candidate skills, experience, behavioral hiring signals, GitHub activity, and availability information to generate explainable and high-quality candidate rankings.

The system produces a ranked list of candidates along with interpretable reasoning for each recommendation.

---

# Problem Statement

Recruiters need an efficient way to identify the most relevant candidates from a large talent pool.

The objective is to:

- Understand job requirements
- Evaluate candidate profiles
- Rank candidates based on relevance
- Generate explainable recommendations
- Produce a Top-N candidate shortlist

---

# Solution Approach

Our solution follows a multi-stage ranking pipeline.

## Stage 1: Candidate Profile Processing

Candidate profiles are analyzed to extract:

- Technical skills
- Experience
- Domain expertise
- Behavioral signals
- GitHub score
- Notice period

---

## Stage 2: Feature Engineering

The following features are generated:

### Skill Match Score
Measures alignment between candidate skills and job requirements.

### Experience Score
Evaluates relevance and duration of professional experience.

### Hiring Signals

Includes:

- Response Rate
- Interview Rate
- Offer Acceptance Rate

These signals help estimate candidate engagement and hiring probability.

### GitHub Score

Used as a proxy for technical activity and engineering engagement.

### Notice Period

Candidates with shorter notice periods are rewarded.

---

## Stage 3: Candidate Scoring

Multiple signals are combined into a single ranking score.

Example weighting strategy:

| Feature | Weight |
|----------|----------|
| Skill Match | 40% |
| Experience | 25% |
| Interview Rate | 15% |
| Offer Acceptance | 10% |
| GitHub Score | 5% |
| Notice Period | 5% |

The final score determines candidate ranking.

---

# Ranking Methodology

The ranking workflow consists of:

1. Parse candidate information
2. Extract relevant features
3. Normalize feature values
4. Calculate weighted scores
5. Generate candidate explanations
6. Sort candidates by final score
7. Produce ranked output

---

# Explainability

For every recommended candidate, the system generates human-readable reasoning.

Example:

> 6.9 years of experience. Strong match in NLP, RAG, QLoRA, Pinecone, and LlamaIndex. High interview success rate and strong hiring signals.

This improves recruiter trust and transparency.

---

# Data Validation

The solution includes:

- Missing value handling
- Score normalization
- Invalid value correction
- Safe handling of unavailable features
- Consistent ranking generation

---

# End-to-End Workflow

Job Description
↓
Feature Extraction
↓
Candidate Evaluation
↓
Signal Scoring
↓
Weighted Ranking
↓
Explainability Generation
↓
Top Candidate Recommendations

---

# Technologies Used

- Python
- Pandas
- NumPy
- Google Colab
- GitHub

---

# Repository Structure

```text
├── candidate_ranking.ipynb
├── submission.csv
├── README.md
└── assets/
```

---

# Output

The final output contains:

- Candidate ID
- Rank
- Score
- Recommendation Reasoning

Example:

| Candidate ID | Rank | Score |
|-------------|------|--------|
| CAND_0086022 | 1 | 0.8474 |
| CAND_0011687 | 2 | 0.8236 |
| CAND_0045862 | 3 | 0.7974 |

---

# Key Highlights

✅ Multi-factor candidate evaluation

✅ Explainable recommendations

✅ Behavioral signal integration

✅ Recruiter-friendly ranking output

✅ Scalable candidate scoring pipeline

---

# Future Improvements

- Learning-to-Rank models
- Transformer-based semantic matching
- Dynamic weight optimization
- Real-time recruiter feedback loops
- Advanced explainability dashboards

---

# Submission Assets

- Source Code (Jupyter Notebook)
- Ranked Candidate Output File
- Presentation Deck (PDF)
- GitHub Repository

---

# Author

**Harshit Marskole**

M.Tech (Industrial Engineering & Operations Research)  
Indian Institute of Technology Delhi (IIT Delhi)

---

# Thank You

TalentLens AI
