# Open-source multi-lingual speech-to-image project

## Objective:
Given that:
- Visual art is a foundational form of human self-expression
- Speech is the foundational form of human communication
- Not everyone is literate
- Not everyone is sufficiently skilled or confident to generate visual art through traditional or digital media

And in particular:
- Not everyone is a native English speaker
- The most powerful AI text-to-image generation models are based on exclusively English-language prompts

Therefore:
- This project intends to provide a means for anyone to generate visual art directly through their speech, without presumption or prejudice with regard to their native language or level of literacy.

## Pipeline:
- Speech input to notebook: [`IPyWebRTC`](https://ipywebrtc.readthedocs.io/)
- Spoken language detection: OpenAI's [`whisper`](https://github.com/openai/whisper)
- Speech-to-text (speech-to-English): OpenAI's [`whisper`](https://github.com/openai/whisper)
- (English) text-to-image: Stability AI's [`stable-diffusion`](https://huggingface.co/CompVis/stable-diffusion)
  - Locally via [🤗 Diffusers](https://github.com/huggingface/diffusers), or through [DeepAI's API](https://deepai.org/machine-learning-model/stable-diffusion)

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
