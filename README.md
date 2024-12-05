# ML_lab2
# Chatbot Demo with HuggingFace and Gradio

This project demonstrates how to deploy a chatbot using a model hosted on HuggingFace. The interface is built using Gradio, and the code is designed to run on Google Colab with GPU acceleration.

## Features
- **Pre-trained Model Integration:** Load a HuggingFace model to handle conversational input and generate responses.
- **Interactive Interface:** Use Gradio to create a user-friendly chatbot interface.
- **GPU Support:** Utilize Google Colab's GPU for faster inference.

---

## Getting Started


### Setup
1. Open the provided Colab notebook.
2. Install required libraries:
   ```python
   !pip install transformers gradio unsloth
   ```
3. Load the models...
3. Launch the interface:
   ```python
   demo.launch(share=True)
   ```

---

## Improving Model Performance

### **Model-Centric Approach**
To enhance chatbot performance through model improvements:
1. **Hyperparameter Tuning:**
   - Adjust learning rates, batch sizes, and optimizer configurations during fine-tuning.
   - Experiment with different generation parameters such as `max_length`, `temperature`, and `top_k` to balance creativity and coherence.

2. **Model Architecture:**
   - Replace the base model with larger or more advanced architectures (e.g., GPT-3, T5, LLaMA).

3. **Fine-Tuning:**
   - Fine-tune the model on domain-specific data to improve relevance and context understanding.

### **Data-Centric Approach**
Improving the dataset used for training is essential for better results:
1. **Data Augmentation:**
   - Expand the dataset with paraphrased responses or synthetically generated conversations.
   - Use tools like GPT-based augmentation to simulate new, high-quality examples.

2. **Source New Data:**
   - Collect domain-specific data, such as technical support logs, customer queries, or literature.
   - Scrape publicly available conversation datasets that align with your use case.

3. **Clean and Curate Data:**
   - Remove noisy, irrelevant, or duplicate entries.
   - Balance the dataset to ensure diverse responses and reduce bias.

4. **Data Labeling:**
   - Annotate data with metadata (e.g., sentiment, intent) to improve fine-tuning results.

---

## Results of Improvements

Switching to a smaller LLM reduced training time from 24 hours down to approx 11. Also, training for more iterations seemed to decrease the loss. We trained this for one full epoch.

