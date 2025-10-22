# Internship Recommender

![Python](https://img.shields.io/badge/Python-3.11-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-2.2-orange)
![Machine%20Learning](https://img.shields.io/badge/Machine%20Learning-Triplet%20Network-green)
![Smart%20India%20Hackathon](https://img.shields.io/badge/Smart%20India%20Hackathon-2024-purple)
![Status](https://img.shields.io/badge/Status-Core%20AI%20Module-yellow)

---

## 🧠 Overview
This project is an AI system that recommends the **top 5 most relevant government internships** for a candidate based on their skills, experience, and profile.  
It combines **rule-based logic** with **trainable embeddings** using a **Triplet Neural Network**.

The rules help generate intelligent training pairs, while the network learns to understand **skill similarity** and **level compatibility** so it can rank internships more intelligently.

I built this AI system myself for the **Smart India Hackathon (SIH)**.  
Even though the final demo wasn’t end-to-end, the **entire AI + data processing pipeline — from embeddings to TripletNN — was built by me.**

---

## 💡 Why This Matters
Traditional keyword or rule-based matching fails when:
- Skills are written differently (`ML` vs `Machine Learning`)
- Candidates have similar but not identical skill sets  
- Companies use inconsistent terminology  

This model fixes that using embeddings that *learn* relationships between skills.  
It can:
- Understand semantic similarity between skills  
- Match candidates and internships beyond exact text matches  
- Rank opportunities using learned similarity instead of static rules  

---

## 🚀 My Journey
1. **Problem Understanding** — Tasked with building an AI-powered internship recommender.  
2. **Data Preparation** — The dataset was incomplete, so I manually added the `Skills_List` section (with some AI assistance). You can see this in the code — it’s kinda hand-written and chaotic, but it works 😎.  
3. **Rule-Based Pairing** — Built logic to generate **positive** and **negative** pairs using title, location, skill subset, and level constraints.  
4. **Triplet Neural Network** — Designed a 4-layer feed-forward network with **Triplet Margin Loss** for similarity learning.  
5. **Challenges** —  
   - Inconsistent skill names and abbreviations  
   - Sparse level data  
   - Time limits → forced a hybrid of rules + neural embeddings  
6. **Outcome** — A fully functional AI model capable of recommending top 5 internships per candidate — understanding context and similarity, not just text matches.

---

## ⚙️ Technical Details
- **Data** → Candidate profiles + internship descriptions (skills, levels, titles, locations)  
- **Embeddings** → Custom trainable embeddings for skills and experience levels  
- **Model** → 4-layer Triplet Neural Network with ReLU activations  
- **Loss Function** → Triplet Margin Loss  
- **Training** → Positive/negative pairs from hand-coded rules  

> ⚠️ The dataset was incomplete, so parts (like `Skills_List`) were added manually.  
> Despite that, the network still learned meaningful semantic relationships.

---

## 🧩 Current Status
This repo currently includes only the **core AI module**.  
The **user interface and full integration** will be added later.

---

## 🏁 Takeaway
This project blends **rules and deep learning** to tackle a real-world problem — matching candidates to internships.  
It adapts **Triplet Neural Networks (normally used in face recognition)** to the HR/recruitment domain, proving that:
> “With smart embeddings and a bit of chaos, even incomplete data can tell a meaningful story.”

---

⭐ **If you like this project**, drop a star on the repo — I’ll pretend it boosts my confidence. 😅
