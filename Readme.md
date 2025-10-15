# Meeting Transcription + Action Item Extractor

This project provides a complete solution to transcribe meeting audio, generate concise summaries, and extract key decisions and action items using open-source models. It includes an easy-to-use web interface for uploading audio files and viewing the results.

## Demo Video

Click the thumbnail below to watch a 3-5 minute video that demonstrates the project's features and walks through the user interface. 

[![Meeting Summarizer Demo Video](https://www.youtube.com/watch?v=5tjZZYIsnvQ)](https://www.youtube.com/watch?v=5tjZZYIsnvQ)



## What it does

-   **Transcribe Audio**: Accurately converts speech from meeting audio files (supports wav, mp3, m4a, ogg) into a full text transcript using `faster-whisper`.
-   **Summarize Transcripts**: Generates a brief, easy-to-read summary of the meeting's content using an LLM. 
-   **Extract Decisions & Action Items**: Intelligently pulls out key decisions made and specific tasks to be done from the transcript, presenting them in a structured format. 
-   **Web Interface**: Offers a simple frontend built with Gradio to upload audio and view the processed results in separate tabs. 

## Models Used

This project relies exclusively on free, open-source models available on Hugging Face:

-   **Automatic Speech Recognition (ASR)**: `faster-whisper` (utilizing the `small` model) for efficient and accurate transcription. 
-   **Summarization**: `sshleifer/distilbart-cnn-12-6` for creating concise summaries. 
-   **Action/Decision Extraction**: `google/flan-t5-base` for parsing the transcript and extracting structured information based on a specific prompt. 

## How to Run in Google Colab

This notebook is designed to be run directly in Google Colab.

1.  **Open the Notebook**
    -   Upload the `.ipynb` file to your Google Drive and open it with Google Colab.

2.  **Enable GPU Acceleration**
    -   For this notebook to run efficiently, you **must** enable the GPU.
    -   Go to the menu and click **Runtime** -> **Change runtime type**.
    -   In the dropdown menu under "Hardware accelerator," select **T4 GPU**.
    -   Click **Save**.

3.  **Run the Cells**
    -   Run each code cell in order from top to bottom. You can do this by clicking the play button next to each cell or by going to the menu and selecting **Runtime** -> **Run all**.
    -   The first time you run, it will take a few minutes to install the necessary libraries and download the models.

4.  **Use the Application**
    -   Once you run the final cell, a **Gradio** web interface will appear in the cell's output.
    -   Use this interface to upload your audio file, and then click the **"Transcribe & Summarize"** button to get your results.

