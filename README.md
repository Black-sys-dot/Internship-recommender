# Internship-recommender

## Overview
This project is an AI system that recommends the **top 5 most relevant government internships** for a candidate based on their skills, experience, and profile. It combines **simple rule-based logic** with **trainable embeddings** using a **Triplet Neural Network**.  

The rules help generate training pairs, and the network learns to understand skill similarity and level compatibility so it can rank internships intelligently.  

I built this AI part entirely myself for the **Smart India Hackathon (SIH)**. While the team faced challenges in presenting a full end-to-end pipeline, the model and data processing — from embeddings to the TripletNN — were developed by me.

---

## Why This Matters
Simple rule-based matching is limited:  
- Companies describe skills differently (e.g., "ML" vs "Machine Learning").  
- Candidates with similar skills may not match exact keywords.  
- Writing rules for every variation is not scalable.  

This model learns embeddings for skills and levels, so it automatically understands these nuances. It can:  
- Recognize semantic skill similarity.  
- Match candidates to jobs even if the wording differs.  
- Rank internships effectively without manually coding every possibility.

---

## My Journey
1. **Problem Understanding**: Tasked with recommending internships using AI.  
2. **Data Preparation**: The original dataset was incomplete. I added the **Skills_List** section myself, with some help from an AI assistant, to make it usable for training. This part can be seen in the code itself and is a bit hand-crafted.  
3. **Rule-Based Pairing**: Created simple rules to generate positive and negative pairs for training the triplet network (matching title/location, subset of skills, level constraints).  
4. **Triplet Neural Network**: Implemented a 4-layer feed-forward network with triplet margin loss to learn similarity between candidate and internship embeddings.  
5. **Challenges**:  
   - Skill synonyms and abbreviations.  
   - Sparse or inconsistent level/job data.  
   - Limited time, requiring a hybrid AI + rules approach.  
6. **Outcome**: A fully functioning model capable of recommending top 5 internships for any candidate profile, understanding nuanced skill similarity.

---

## Technical Details
- **Data**: Candidate profiles and job postings with skills, levels, titles, and locations. Some parts of the dataset were incomplete, so I added missing skills manually to enable training.  
- **Embeddings**: Trainable skill embeddings and level embeddings.  
- **Model**: Triplet Neural Network with 4 fully connected layers and ReLU activations.  
- **Loss**: Triplet Margin Loss for learning embeddings that bring candidates closer to matching internships and away from non-matching ones.  
- **Training**: Positive/negative pairs generated from simple rules.

---

**Note**: I haven’t built a user interface yet — this is the core AI module. Interface and end-to-end integration will be added later.

---

## Takeaway
This project shows how AI can enhance traditional rule-based matching by learning semantic relationships in skills and experience. It adapts Triplet Neural Networks — usually used for face recognition — to a real-world problem of internship recommendation, proving that smart embeddings + simple rules can solve messy, real-life challenges efficiently.

Even though the dataset was incomplete, and some sections (like Skills_List) were hand-added, the model still demonstrates how embeddings and triplet loss can learn meaningful matches, showing the potential for real-world applications in recruitment platforms.


