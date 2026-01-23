# PersonaPlex on Google Colab

This folder contains a Google Colab notebook that launches the PersonaPlex Web UI.

## Colab badge (for your fork)

Replace `{YOUR_GITHUB}` and `{YOUR_BRANCH}` with your fork info:

https://colab.research.google.com/github/{YOUR_GITHUB}/personaplex/blob/{YOUR_BRANCH}/colab/PersonaPlex_WebUI_Colab.ipynb

## What you get

- A Colab notebook that:
  - installs dependencies (avoiding `sounddevice` which often fails on Colab)
  - authenticates to Hugging Face (required)
  - launches `moshi.server` with a public tunnel URL

## Prerequisites

- A Google Colab runtime with GPU enabled.
- A Hugging Face account.
- You must accept the model license on:
  - https://huggingface.co/nvidia/personaplex-7b-v1

## Run

Open and run:

- `PersonaPlex_WebUI_Colab.ipynb`

The notebook will print a public tunnel URL after the server starts. Open that URL to access the Web UI.

## Notes

- This repository code is MIT licensed. Model weights are under the NVIDIA Open Model License and are not redistributed here.
- The notebook expects you to provide your own Hugging Face token at runtime.
