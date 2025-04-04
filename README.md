# Diarization-with-Custom-dataset
This purpose of this project is to show the performance of some open and closed state of the art models on Diarization task.

# 🗣️ Speech Diarization on Custom Dataset

This project focuses on **speech diarization**—the task of determining "who spoke when"—using a custom dataset. We explore multiple diarization models, both open-source and closed-source, and evaluate their performance using standard diarization metrics.

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
