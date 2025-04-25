# Indian Popular Music Dataset
This repository contains a manually aligned dataset of Indian popular music vocal tracks and their corresponding MIDI files. It is curated for research tasks such as **Automatic Music Transcription (AMT)** and **audio-to-MIDI alignment**.
---

## 📁 Dataset Structure

- **`audio_mp3/`**  
  Contains Indian popular music vocal tracks in MP3 format. Each track is manually trimmed and aligned with the midi files.

- **`ground_truth_midi/`**  
  MIDI files downloaded from [MuseScore](https://musescore.com/), used as ground truth.

---

## 🛠️ Dataset Preparation and Manual Alignment
The MP3 audio tracks were not originally synchronized with the MIDI files. To ensure meaningful model training and evaluation, each audio file was manually aligned with its corresponding MIDI track. Below are the steps followed:

### 🎬 Step-by-Step Alignment Using Adobe Premiere Pro

1. **Import Both Files**
   - Open Adobe Premiere Pro.
   - Import the MP3 vocal track and the corresponding MIDI file.

2. **Create a Timeline**
   - Create a new sequence and place both tracks on separate layers in the timeline.

3. **Manual Trimming & Syncing**
   - Play both tracks simultaneously.
   - Identify leading silence or extra instrumental intros in the MP3 file.
   - Trim the MP3 track so that the onset of the vocal matches the starting point of the MIDI melody.
   - Use waveforms to visually match peaks in the audio and MIDI reference.
   - Use zoom-in tools for precise alignment.

4. **Export Aligned Audio**
   - Once aligned, export the trimmed audio as a new .mp3 file using the same name as the MIDI file for consistency..

---

### 👀 Visualizing Alignment Using Sonic Visualiser

1. **Open Sonic Visualiser**
   - Load the trimmed MP3 audio file.

2. **Import MIDI Layer**
   - Go to `File → Import Layer → MIDI File`.
   - This will display MIDI note events as overlays on the waveform.

3. **Inspect Alignment**
   - Ensure that note onsets and transitions in the MIDI layer visually and audibly match the MP3 waveform.
   - Use zoom and playback to verify precision.

---

## 📌 Use Cases

- Training and evaluation of AMT systems
- Time-aligned vocal melody extraction
- Research in audio-visual music learning

---

## 🙏 Acknowledgments

- MIDI files obtained from [MuseScore](https://musescore.com/)
- Alignment and editing tools used:
  - Adobe Premiere Pro
  - Sonic Visualiser

---


