# Conversational AI & Image Generation Demos

This repository contains Jupyter notebooks and supporting files for experimenting with conversational AI (chatbots) and image generation using large language models (LLMs) and APIs such as OpenAI, Hugging Face, and Gradio.

## Repository Structure

- **day3.ipynb**: Main notebook for building and experimenting with a conversational AI assistant (chatbot) using OpenAI's API and Gradio for the user interface.
- **airline-agent.ipynb**: Notebook for an airline-related chatbot or agent.
- **image_generation.ipynb**: Notebook for generating images using state-of-the-art diffusion models and transformer libraries.
- **environment.yml**: Conda environment file listing dependencies for easy setup.
- **.ipynb_checkpoints/**: Jupyter auto-saved notebook checkpoints.
- **.vscode/**: VS Code workspace settings.

## Setup

1. **Clone the repository**
   ```sh
   git clone <repo-url>
   cd <repo-directory>
   ```

2. **Create and activate the environment**
   ```sh
   conda env create -f environment.yml
   conda activate <env-name>
   ```

3. **Set up API keys (if required)**
   - Create a `.env` file in the root directory with your API keys:
     ```
     OPENAI_API_KEY=your_openai_key
     ANTHROPIC_API_KEY=your_anthropic_key
     GOOGLE_API_KEY=your_google_key
     ```

## Notebooks Overview

### Conversational AI

- **day3.ipynb**: Demonstrates building a context-aware chatbot for a clothing store, including prompt engineering and handling special cases (e.g., items not on sale). Uses Gradio for a web-based chat interface and streams responses from OpenAI's API.
- **airline-agent.ipynb**: Example chatbot for airline customer service scenarios.

### Image Generation

- **image_generation.ipynb**: 
    - Demonstrates how to generate images using Hugging Face's `diffusers` and `transformers` libraries.
    - Supports accelerated inference with `accelerate` and `bitsandbytes`.
    - The first cell installs all necessary packages:
      ```python
      # Disregard the error that pip gives you when you run this - all should be well!
      !pip install -q diffusers transformers accelerate bitsandbytes datasets==3.6.0 fsspec==2023.9.2
      ```
    - Follow the notebook instructions to generate images using your preferred models.
    - **Note:** You may need a GPU for best performance with diffusion models.

## Requirements

- Python 3.11+
- Jupyter Notebook or VS Code
- OpenAI, Gradio, Hugging Face libraries, and other dependencies listed in `environment.yml`

## License

This project is for educational purposes.

---

Feel free to modify the notebooks or environment as needed for your own experiments!