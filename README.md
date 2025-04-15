# Text Summary Web Application

A Streamlit web application for extracting and summarizing content from web pages.

## Features

- Extract readable content from any web URL
- Process content using LLM (either Ollama locally or OpenAI API in the cloud)
- Clean and display web content with a user-friendly interface

## Local Development Setup

### Prerequisites

- Python 3.11 or higher
- Ollama (for local LLM processing)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/text-summary-app.git
   cd text-summary-app
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Install Ollama:
   - Visit [https://ollama.com/download](https://ollama.com/download)
   - Follow the installation instructions for your platform

4. Pull the required model:
   ```bash
   ollama pull llama2-uncensored
   ```

5. Run the application:
   ```bash
   streamlit run textsummary_app.py
   ```

## Deployment Options

### Option 1: Streamlit Cloud (Easiest)

1. Push your code to GitHub
2. Create an account on [Streamlit Cloud](https://streamlit.io/cloud)
3. Connect your GitHub repository
4. Use the `cloud_textsummary_app.py` version that works with OpenAI API
5. Set up your OpenAI API key in Streamlit Cloud secrets

### Option 2: Hugging Face Spaces

1. Create an account on [Hugging Face](https://huggingface.co/)
2. Create a new Space with Streamlit SDK
3. Use the `cloud_textsummary_app.py` version that works with OpenAI API
4. Configure secrets in the Hugging Face Spaces UI

### Option 3: Self-hosted on a VM (Digital Ocean, AWS, GCP)

1. Create a VM on your preferred cloud provider
2. SSH into your VM
3. Run the deployment script:
   ```bash
   chmod +x deploy_vm.sh
   ./deploy_vm.sh
   ```
4. Configure a domain name to point to your VM's IP address

### Option 4: Docker Deployment

1. Build the Docker image:
   ```bash
   docker build -t text-summary-app .
   ```

2. Run the container:
   ```bash
   docker run -p 8501:8501 text-summary-app
   ```

## Using Cloud APIs Instead of Ollama

If you prefer to use OpenAI API instead of Ollama for deployment simplicity:

1. Create a `.streamlit/secrets.toml` file with your OpenAI API key:
   ```toml
   OPENAI_API_KEY = "your-openai-api-key-here"
   ```

2. Use the `cloud_textsummary_app.py` version:
   ```bash
   streamlit run cloud_textsummary_app.py
   ```

## Customization

You can customize the application by:

1. Changing the LLM model in the code
2. Modifying the prompts for different extraction behavior
3. Adjusting the UI in the Streamlit app code

   
# text-extractor
