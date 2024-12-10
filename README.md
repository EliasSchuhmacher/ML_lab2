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

2. **Model Architecture:**
   - Replace the base model with larger or more advanced architectures (e.g., GPT-3, T5, LLaMA).
   - In our case, due to limitations in computing power, we wanted to reduce the training time.
     We did this by switching to a smaller base model, Llama-3.2 1B instead of 3B. This reduced training time from 25h39m down to 12h27m


### **Data-Centric Approach**
Improving the dataset used for training is essential for better results:
1. **Data Augmentation:**
   - Expand the dataset with paraphrased responses or synthetically generated conversations.
   - Use tools like chat-GPT or other advanced LLMs to simulate new, high-quality examples.

2. **Source New Data:**
   - We could also use a larger instructional dataset such as fulltome, which contains a lot more samples. This is likely to increase model performance

3. **Clean and Curate Data:**
   - Remove noisy, irrelevant, or duplicate entries.


---

## Results of Improvements

Switching to a smaller LLM reduced training time from 25 hours down to approx 12. Also, training for more iterations seemed to decrease the loss. During testing we only trained for 60 steps, which resulted in the loss still being pretty high. We trained this for one full epoch, and loss seemed to decrease with increasing number of training steps.

