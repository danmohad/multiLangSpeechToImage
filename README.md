# Open-source multi-lingual speech-to-image project

## Pipeline:
- Speech input to notebook: [`IPyWebRTC`](https://ipywebrtc.readthedocs.io/)
- Spoken language detection: OpenAI's [`whisper`](https://github.com/openai/whisper)
- Speech-to-text (speech-to-English): OpenAI's [`whisper`](https://github.com/openai/whisper)
- (English) text-to-image: Stability AI's [`stable-diffusion`](https://huggingface.co/CompVis/stable-diffusion) via [🤗 Diffusers](https://github.com/huggingface/diffusers)

## Basic requirements:
- Python v3.10.6
- An account on [🤗 (Hugging Face)](https://huggingface.co/)
  - Must accept T&C before downloading the [`stable-diffusion` weights](https://huggingface.co/runwayml/stable-diffusion-v1-5)
- `ffmpeg`
  - Can install via `brew`, `apt`, `conda` or other package manager
  
## Installation:
- Create and activate a fresh python v3.10.6 `venv`
- `git clone` this repository
- Install the dependencies with `pip install -r requirements.txt`
- Download the `stable-diffusion` weights
  - `git lfs install`
  - `git clone https://huggingface.co/runwayml/stable-diffusion-v1-5`
