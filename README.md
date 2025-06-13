This repo contains a Python Google Colab file, as well as the PowerPoint presentation explanation and Proposal report.

## About the Dataset

### Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS)

This dataset contains speech audio-only files from the RAVDESS collection, provided in 16-bit, 48kHz `.wav` format. The complete dataset—including speech and song, audio and video (24.8 GB)—is available from [Zenodo](https://zenodo.org/). Details about the construction and perceptual validation of the RAVDESS can be found in the [Open Access paper in PLoS ONE](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0196391).

For song emotion data, check out our [Kaggle Song Emotion Dataset](https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-song-audio).

---

### Dataset Structure

- **Total Files:** 1,440 audio files  
  (`60 trials per actor × 24 actors = 1,440`)
- **Actors:** 24 professional actors (12 female, 12 male)
- **Statements:** Two lexically-matched statements, spoken in a neutral North American accent.
    - "Kids are talking by the door"
    - "Dogs are sitting by the door"
- **Emotions:** Calm, Happy, Sad, Angry, Fearful, Surprised, Disgust, and Neutral
    - Each (except Neutral) is expressed at two intensity levels: normal and strong

---

### File Naming Convention

Each file is named using a 7-part numerical identifier, e.g., `03-01-06-01-02-01-12.wav`, which encodes the following characteristics:

| Position | Value(s) | Description |
|----------|----------|-------------|
| 1        | 01, 02, 03 | Modality (01 = full-AV, 02 = video-only, 03 = audio-only) |
| 2        | 01, 02     | Vocal Channel (01 = speech, 02 = song) |
| 3        | 01–08      | Emotion (01 = neutral, 02 = calm, 03 = happy, 04 = sad, 05 = angry, 06 = fearful, 07 = disgust, 08 = surprised) |
| 4        | 01, 02     | Emotional Intensity (01 = normal, 02 = strong) <br> *Note: No strong intensity for 'neutral' emotion* |
| 5        | 01, 02     | Statement (01 = "Kids are talking by the door", 02 = "Dogs are sitting by the door") |
| 6        | 01, 02     | Repetition (01 = 1st repetition, 02 = 2nd repetition) |
| 7        | 01–24      | Actor (01 to 24; odd = male, even = female) |

**Example:**  
`03-01-06-01-02-01-12.wav`  
- `03` = Audio-only  
- `01` = Speech  
- `06` = Fearful  
- `01` = Normal intensity  
- `02` = Statement: "Dogs are sitting by the door"  
- `01` = 1st repetition  
- `12` = 12th actor (female; even number)  

---

### Summary Table

| Attribute          | Values / Range                                        |
|--------------------|------------------------------------------------------|
| Modality           | 01 = full-AV, 02 = video-only, 03 = audio-only       |
| Vocal channel      | 01 = speech, 02 = song                               |
| Emotion            | 01 = neutral, 02 = calm, 03 = happy, 04 = sad, 05 = angry, 06 = fearful, 07 = disgust, 08 = surprised |
| Emotional Intensity| 01 = normal, 02 = strong (no strong for neutral)     |
| Statement          | 01 = "Kids are talking by the door", 02 = "Dogs are sitting by the door" |
| Repetition         | 01 = 1st, 02 = 2nd                                   |
| Actor              | 01–24 (odd = male, even = female)                    |

---

**References:**
- [RAVDESS on Zenodo](https://zenodo.org/record/1188976)
- [PLoS ONE RAVDESS Paper](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0196391)
- [Kaggle Song Emotion Dataset](https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-song-audio)
