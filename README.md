# Group 9 AI Video Transcriber
Overview: Our project uses GenAI-driven video caption generation and content summarization. It automatically extracts audio from video files and transcribes them using OpenAI's Whisper model. 

Contributers:
Aziz BinAbid - Project manager, Resarcher
Sean Meyers - Researcher, Workflow Testing
Ashton Emeigh - Researcher, Writer/Editor

Project Details
- Video audio becomes the generative prompt
- Uses multiple models such as Whisper and Stable Diffusion
- Uses automated preprocessing taking a video and extracting available audio
- Has API service integration such as Hugging Face, ngrok, Streamlit, and MoviePy
- Maintains error handling when taking Ngrok token and handling video transcription

Project Description
Manual video captioning is time consuming and error-prone. Additionally, it is generally not scalable for mass content
creation. The goal is to make a system that automatically transcribes audio from real world video uploads using GenAI models.
Additionally, the model can create short summaries of the content depending on the user request.

Models Used
- OpenAI Whisper, used for speach recognition and converts audio to text caption
- Stable Diffusion v1.5 (Diffusers), used for transcript as a prompt to generate images if requested by user (optional)
- Streamlit for deployment and UI rendering to handle user interactions
- Ngrok for tunneling to expose streamlit to user via the internet

Dataset
Our project does not use a preloaded dataset but instead processes real-world user media.

System Architecture
- User Upload (audio/video file through Streamlit)
- Preprocesses, saves the file locally and extracts audio via moviepy
- Whisper ASR, transcribes the video audio to text
- Output, displays the caption text and stores the transcript as a prompt

Component Architecture
- Streamlit UI, handles file upload, error messages, and output
- Processing/Backend Logic, saves the file detects file type, then extracts the audio
- AI Model Integration, Whisper (via Hugging Face), Diffuser and Transformers
- Deployment Layer, Google Colab and ngrok tunnel to internet
