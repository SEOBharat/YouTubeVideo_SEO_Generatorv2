# YouTube Video SEO Analysis Script

This Python script is designed to streamline the process of extracting insights from YouTube videos and generating SEO-optimized content such as titles, meta descriptions, keywords, and full descriptions. Using OpenAI's Whisper API for audio transcription and GPT for content analysis, the script is ideal for SEOs and digital marketers.

## Features
1. **Audio Extraction**: Extracts audio from YouTube videos using `yt-dlp`.
2. **Transcription**: Converts audio into text using OpenAI Whisper API.
3. **SEO Analysis**: Analyzes transcripts to generate:
    - SEO-optimized title (under 60 characters).
    - Meta description (under 160 characters).
    - Relevant keywords.
    - Full SEO-optimized description.
4. **Output**: Saves all data, including the original video metadata and analysis, into an Excel file.

---

## Prerequisites

### Install Required Packages
Ensure you have Python installed and the following libraries:

```bash
pip install openai pandas requests yt-dlp
```

### OpenAI API Key
Set your OpenAI API key in the script by replacing:
```python
client = OpenAI(api_key="Your-OpenAI_API_Key")
```

---

## Usage Instructions

1. **Prepare Input Excel File**:
   - Create an Excel file named `input_videos.xlsx`.
   - The file must contain the following columns:
     - `Page URL`
     - `Page Title`
     - `Meta description`
     - `YouTube Video URL` (mandatory).

2. **Run the Script**:
   - Save the script as `youtube_seo_analysis.py`.
   - Execute the script:
     ```bash
     python youtube_seo_analysis.py
     ```

3. **Output File**:
   - The script generates an output Excel file named `video_analysis_results.xlsx`.
   - This file includes:
     - Original metadata (Page URL, Page Title, Meta description).
     - SEO Analysis (SEO Title, Meta Description, Keywords, Full Description).

---

## Script Workflow
1. **Audio Extraction**:
   - Uses `yt-dlp` to download audio from YouTube.
2. **Transcription**:
   - Transcribes the audio to text via OpenAI Whisper API.
3. **SEO Analysis**:
   - Processes the transcript using GPT to generate SEO content.
4. **Results Compilation**:
   - Outputs all data into an organized Excel sheet.

---

## Troubleshooting
- **Transcription Fails**:
  - Ensure the Whisper API key is correct.
  - Check audio quality of the video.
- **Missing Columns**:
  - Verify that the input Excel includes the required columns.
- **API Errors**:
  - Ensure the OpenAI API key has sufficient usage limits.

---

## Limitations
1. The script assumes all YouTube videos are accessible and have transcribable audio.
2. Ensure your OpenAI API key supports the Whisper and GPT models.
3. API usage costs may apply.

---

## Contribution
Feel free to fork the repository, submit issues, or propose improvements via pull requests.

---

## License
This project is licensed under the MIT License. See the LICENSE file for details.

