# Open-source multi-lingual speech-to-image project

## Pipeline:
- Speech input to notebook: [`IPyWebRTC`](https://ipywebrtc.readthedocs.io/)
- Spoken language detection: OpenAI's [`whisper`](https://github.com/openai/whisper)
- Speech-to-text (speech-to-English): OpenAI's [`whisper`](https://github.com/openai/whisper)
- (English) text-to-image: Stability AI's [`stable-diffusion`](https://huggingface.co/CompVis/stable-diffusion) via [🤗 Diffusers](https://github.com/huggingface/diffusers)

## Requirements:
- Python v3.10.6
