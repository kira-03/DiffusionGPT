

# **Text-to-Image Generation System: Fine-Tuned AI for Creative Visuals**

This repository presents our custom **Text-to-Image Generation System**, designed as part of a Natural Language Processing (NLP) course project. The system combines state-of-the-art models for generating high-quality images from textual descriptions and includes a custom prompt generation module for creative input.

---

## **Table of Contents**

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Setup](#setup)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Prompt Generation](#prompt-generation)
  - [Image Generation](#image-generation)
- [Interactive Feedback Loop](#interactive-feedback-loop)
- [Enhancements and Future Work](#enhancements-and-future-work)
- [License](#license)

---

## **Overview**

### Phase 1: Case Study on DiffusionGPT
In the initial phase of this project, we conducted an in-depth review of **DiffusionGPT**, a text-to-image generation system described in the research paper ([arXiv:2401.10061](https://arxiv.org/pdf/2401.10061)). This review provided insights into the capabilities and limitations of text-to-image models, forming the basis for our implementation phase.

### Phase 2: Custom Implementation
Building upon our findings, we developed a fine-tuned text-to-image generation system that integrates:
- A **custom prompt generation model** for crafting concise and creative descriptions.
- Advanced **Stable Diffusion** pipelines for generating visually appealing images.
- A dynamic **user feedback loop** for iterative refinement of image outputs.

This system showcases the potential of combining prompt engineering, generative AI, and user interaction for seamless text-to-image workflows.

---

## **Features**

- **Custom Prompt Generator**:
  - Generates creative prompts with concise descriptions optimized for image generation.
  - Enhances user inputs with atmospheric and stylistic details for richer results.

- **High-Quality Image Generation**:
  - Leverages Stable Diffusion for ultra-detailed, aesthetically pleasing outputs.

- **Interactive Feedback Loop**:
  - Enables users to refine image generation parameters iteratively for optimal results.

- **Post-Processing**:
  - Enhances images with contrast and sharpness adjustments for improved visual quality.

---

## **Architecture**

### 1. **Prompt Generation**:
   - Uses a GPT-2-based module to craft meaningful prompts, incorporating key details, moods, and artistic styles.

### 2. **Text-to-Image Generation**:
   - Integrates Stable Diffusion to produce high-resolution images from textual inputs.
   - Augments prompts with descriptors like "high quality" and "cinematic lighting" for superior results.

### 3. **Interactive Feedback**:
   - Includes a feedback loop where users can fine-tune parameters such as guidance scale and inference steps.

### 4. **Post-Processing**:
   - Applies contrast and sharpness enhancements to improve output quality.

---

## **Setup**

### Prerequisites

- Python 3.7 or higher
- GPU with CUDA support (recommended for faster processing)
- Libraries: PyTorch, Transformers, diffusers, Pillow, matplotlib

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/Text-to-Image-Generation-System.git
   cd Text-to-Image-Generation-System
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # For Linux/Mac
   venv\Scripts\activate     # For Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. (Optional) Verify GPU availability:
   ```python
   import torch
   print(torch.cuda.is_available())  # Should return True if GPU is available
   ```

---

## **Usage**

### Prompt Generation

Run the prompt generation module to craft creative inputs:
```bash
python prompt_generator.py
```

You will be prompted to provide:
- Subject (e.g., "a crystal palace")
- Environment (e.g., "floating in clouds")
- Mood (e.g., "mysterious")
- Key Details (e.g., "light fragments through crystal walls")
- Action (e.g., "ethereal beings glide through halls")
- Art Style (e.g., "dreamlike watercolor")

The output will be a concise and creative image description optimized for text-to-image generation.

### Image Generation

Run the main pipeline:
```bash
python main.py
```

1. Provide a textual description as input.
2. The system generates an image based on the input and displays it.
3. If unsatisfied, you can adjust parameters interactively and regenerate the image.

---

## **Interactive Feedback Loop**

1. **View the Image**:
   - The system displays the generated image after each iteration.
   
2. **Provide Feedback**:
   - Choose whether you are satisfied with the result:
     - **Yes**: Saves the image and exits.
     - **No**: Allows you to adjust the guidance scale and inference steps for refinement.

---

## **Enhancements and Future Work**

- **Expand Prompt Diversity**:
  - Include more artistic styles, moods, and detailed descriptors.

- **Optimize Models**:
  - Explore lightweight model adaptations for faster inference.
  
- **Batch Processing**:
  - Add support for generating multiple images simultaneously.

- **User Interface**:
  - Build a web-based interface for seamless interaction.

---

## **License**

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## **Acknowledgments**

We extend our gratitude to:
- OpenAI for GPT-2 and CLIP models.
- Hugging Face for their powerful library ecosystem.
- Stability AI for the Stable Diffusion pipeline.

For more details on the case study, refer to the [DiffusionGPT research paper](https://arxiv.org/pdf/2401.10061).

---

Feel free to adjust this as needed. Let me know if you'd like help with further customizations!
