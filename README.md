# DarkIntern

## Project Overview

This project is based on the **InternLM2.5 series model** and aims to create a generative dialogue system with a dark, rebellious style. By combining **Retrieval-Augmented Generation (RAG)** technology, have built a model capable of generating dialogue filled with villainous traits, such as threats, provocation, and coldness. The system retrieves relevant text information from a pre-constructed knowledge base, enriching its outputs with variety and depth.

## Key Features

- **Dark Style Dialogue Generation**: The model generates responses with a dark, villainous tone, suitable for applications in games, movies, novels, etc.
- **RAG-Enhanced Generation**: By incorporating external knowledge sources, the model's responses are more diverse and insightful.
- **Customizable Dialogue Style**: This model is particularly well-suited for users interested in villainous characters, dark philosophy, historical figures, or similar themes.

## Quick Start

### 1. Clone the Repository

First, clone the project to your local machine:

git clone https://github.com/yourusername/DarkIntern.git

### 2. Prepare the Data

Place the villain quotes, dark novel excerpts, and other relevant data in the `data/` folder. Ensure the format of the data is suitable for model training. If you don't have an existing dark dataset, you can gather data from public resources or write your own.

### 3. Train the Model (Optional)

If you need to fine-tune the model, you can use the `train.py` script. Run the following command to begin training:

python scripts/train.py --datadir data/ --outputdir model/ --batch_size 16 --epochs 3

This command will fine-tune the model using the training data in the `data/` directory and save the trained model in the `model/` folder.

### 4. Use the Model to Generate Dialogue

After training the model, you can generate dialogue with a dark, villainous style using the `generate.py` script. You can provide a prompt or situation, and the model will generate a response with a villainous tone.

python scripts/generate.py --model_dir model/ --input "What do you think the ultimate fate of humanity will be?"

### 5. RAG Retrieval Enhancement

When generating dialogue, the model retrieves relevant villainous-style text based on the input. You can use the `retrieve.py` script to query the retrieval database:

python scripts/retrieve.py --query "How do villains view heroes?" --indexdir data/retrievaldata/

## Example Usage

### Example 1: Dialogue Generation

python scripts/generate.py --model_dir model/ --input "If you were the ruler of the world, what would you do?"

Output:
“The world? It’s nothing but floating dust. I will make all bow before me in fear; their fear is the proof of my existence.”

### Example 2: RAG Retrieval and Generation

python scripts/generate.py --model_dir model/ --input "How does one become a villain?"

Output:
“First, you must cast aside all moral constraints. Then, you must learn to manipulate others' fears, becoming their darkest nightmare.”
