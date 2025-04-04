# Diarization-with-Custom-dataset
This purpose of this project is to show the performance of some open and closed state of the art models on Diarization task.

# 🗣️ Speech Diarization on Custom Dataset

This project focuses on **speech diarization**—the task of determining "who spoke when"—using a custom dataset. We explore multiple diarization models, both open-source and closed-source, and evaluate their performance using standard diarization metrics.

# 🧠 Understanding Diarization and Diarization Error Rate (DER)

## 🗣️ What is Speech Diarization?

**Speech diarization** is the process of segmenting an audio stream to determine "**who spoke when**." It is essential in applications like meeting transcription, conversational analysis, and speaker indexing, especially when multiple speakers are involved.

---

## 📐 Foundational Concepts and Mathematics Behind Diarization

Speech diarization typically consists of several stages, each grounded in mathematical principles:

### 1. Voice Activity Detection (VAD)

**Goal:** Identify time segments that contain speech.

This is often modeled as a binary classification problem:


Neural networks trained on acoustic features like MFCCs or log-mel spectrograms are commonly used.

---

### 2. Speaker Embedding Extraction

Each speech segment is converted into a **vector representation** (embedding) that captures speaker characteristics.



y_i = 
\begin{cases}
1, & \text{if frame } i \text{ contains speech} \\
0, & \text{otherwise}
\end{cases}



Where:
- `T_ref` = Total reference speaker time
- `T_miss` = Time missed (not detected)
- `T_fa` = Time falsely detected as speech
- `T_err` = Time attributed to the wrong speaker

---

### Example

If:
- `T_ref = 100` seconds  
- `T_miss = 5` seconds  
- `T_fa = 3` seconds  
- `T_err = 7` seconds  

Then:


---

## 📁 Project Structure

```bash
.
├── README.markdown
├── data/
│   ├── raw/                # Raw custom audio files (WAV, MP3, etc.)
│   ├── annotations/        # Reference speaker segments in RTTM or CSV
├── notebooks/
│   ├── preprocess_data.ipynb
│   ├── run_diarization.ipynb
│   ├── evaluate_models.ipynb
├── models/
│   ├── pyannote/
│   ├── resemblyzer/
│   ├── whisperx/
│   ├── closed_model_X/     # Placeholder for commercial models (e.g., AssemblyAI, Rev.ai)
├── scripts/
│   ├── diarize.py          # Script for running diarization model
│   ├── evaluate.py         # Calculate DER and other metrics
├── results/
│   ├── diarization_outputs/
│   ├── evaluation_reports/
