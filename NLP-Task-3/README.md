# Console-Based Chatbot with Hugging Face Transformers

This project demonstrates a simple, continuous console-based chatbot implemented in a Jupyter Notebook. It leverages Hugging Face's `transformers` library and PyTorch to generate conversational responses using Microsoft's pre-trained `DialoGPT-medium` model.

## Features
- **Continuous Conversation Context**: The chatbot retains conversation history across turns, allowing for contextual and natural back-and-forth interactions.
- **Pre-trained Conversational Model**: Uses `microsoft/DialoGPT-medium`, a model fine-tuned specifically for human-like dialogue generation.
- **Console Interface**: A simple while-loop interface using Python's native `input()` function for seamless chatting directly within the notebook's output cell.
- **Graceful Exit**: Built-in commands (`exit` or `quit`) to safely terminate the conversation loop.

## Prerequisites
Ensure you have Python installed. You will need to install the following libraries to run the notebook:
- `transformers`
- `torch` (PyTorch)

You can install them via the first cell of the notebook or by running:
```bash
pip install transformers torch
```

## How to Run
1. Open the `Chatbot.ipynb` file in Jupyter Notebook, JupyterLab, or VS Code.
2. Run **Cell 1** to install the required dependencies (if you haven't already).
3. Run **Cell 2** to import the libraries and download/load the `DialoGPT-medium` model and tokenizer. *(Note: This might take a moment on the first run as it downloads the model weights).*
4. Run **Cell 3** to start the chatbot interaction loop.

## Usage
Once the chatbot interface is running, you will see a prompt like this:
```
Chatbot: Hello! I am your AI assistant. How can I help you today?
User: 
```
Type your message and press **Enter** to chat!

To end the session, type exactly `exit` or `quit` (case-insensitive).

## Technical Details
- **Tokenization**: Uses `AutoTokenizer` and handles the BPE tokenizer clean-up space warning automatically.
- **Generation Parameters**:
  - `max_length=1000`: Caps the total length of the conversation history tensor.
  - `no_repeat_ngram_size=3`: Prevents the bot from repeating the exact same phrases.
  - `do_sample=True`, `top_k=50`, `top_p=0.95`, `temperature=0.7`: Tuned hyper-parameters for creative, dynamic, yet coherent human-like responses.
