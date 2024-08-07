# Academic Research Chatbot

This project utilizes a chatbot built using the `langchain` library and a Hugging Face model fine-tuned on academic research papers. The chatbot is designed to provide knowledgeable and helpful responses to user queries, leveraging advanced AI techniques.

## Requirements

- Python 3.7 or higher
- `gradio`
- `langchain`
- `langchain_huggingface`
- `transformers`

You can install the required libraries using pip:

```bash
pip install gradio langchain langchain_huggingface transformers
```
**Interact with the Chatbot**:

   - Enter your question in the chat interface.
   - The chatbot will respond with a knowledgeable and informative answer based on its training on academic research papers.

## Model Details

The model used in this project is `VMware/flan-t5-large-alpaca`, fine-tuned specifically on academic research papers. This fine-tuning process enhances the model's ability to provide accurate and detailed responses to academic and research-related queries.

## Code Explanation

- **Imports**: The script imports necessary libraries including Gradio for the user interface, `langchain` for building the chatbot, and `transformers` for model loading.
  
- **Pipeline Setup**:
  - The `pipeline` function from the `transformers` library is used to load the `VMware/flan-t5-large-alpaca` model for text generation.
  - The `HuggingFacePipeline` from `langchain_huggingface` integrates this model with `langchain`.

- **Prompt Template**: 
  - A prompt template is created to guide the chatbot's responses, ensuring it behaves as a knowledgeable and helpful AI assistant.

- **LLM Chain**: 
  - `LLMChain` from `langchain` is used to connect the model with the prompt template, allowing for dynamic generation of responses.

- **Chatbot Function**: 
  - The `chatbot` function takes a user's question and generates a response using the LLM chain.

- **Gradio Interface**:
  - `gr.ChatInterface` is used to create a simple web interface for interacting with the chatbot.
  - It provides an easy-to-use chat interface for entering questions and displaying responses.
