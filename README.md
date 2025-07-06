# 🧠 AI Comic Strip Generator

Turn any short story into a sequence of comic-style images using NLP and text-to-image generation.

---

## 📌 Project Summary

This project transforms a short narrative into illustrated scenes by:
1. **Splitting the story into scenes** using NLP & clustering
2. **Enhancing each scene** with artistic and visual context
3. **Generating AI art** from prompts using a text-to-image model


## 🧰 Tech Stack

| Layer | Tools |
|-------|-------|
| NLP | `nltk`, `sentence-transformers` |
| Clustering | `KMeans`, `Agglomerative`, `HDBSCAN` |
| Prompt Design | Custom rule-based enhancer |
| Image Gen | `DALL·E` / `diffusers` (`Stable Diffusion`) |
| UI / Notebook | `Colab` / `Streamlit` (optional) |

---

## 📖 How It Works

1. **Scene Splitting**
   - Tokenize → Embed (MPNet) → Cluster sentences into scenes
   - Evaluated with **Silhouette Score**:
     ```
     KMeans Score: 0.02
     Agglomerative Score: 0.10
     ```

2. **Prompt Enhancement**
   - Adds artistic detail using random styles and fantasy elements:
     ```
     A robot awakens in a ruined city, featuring a hooded wizard, set in an alien landscape, cinematic lighting.
     ```

3. **Image Generation**
   - Each prompt sent to an AI image model to render as a comic panel

---

## 📈 Experiments

| Method         | Clusters | Silhouette Score |
|----------------|----------|------------------|
| KMeans         | 3        | 0.02             |
| Agglomerative  | 3        | 0.10             |
| HDBSCAN        | auto     | N/A              |

> Despite low silhouette scores, scenes were **semantically valid and visually diverse** after chunking.

---

## 📁 Folder Structure
Colab.py


## 📌 Possible Improvements
- Fine-tune your own style model (e.g., comic diffusion)
- Add BLEU score to evaluate scene-prompt consistency
- Deploy as Streamlit comic strip generator
