# Chatbot-for-mental-health-using-Llama2

## Objective:

Build a chatbot that can assist users with their mental health queries.

## Solution:

1. Use DSM-5 pdf as the data source. Vectorize the data using sentence transformer and store the vectors in pinecone vector database.
2. Use prompts and quantized Llama2 model to take user query and search for the answer in the knowledge base.
3. Build a simple web app using flask for the chatbot


## Techstack Used:

- Python
- Pinecone Vector database
- Meta Llama2
- LangChain
- Flask


## Project Architecture:
![LLM](https://github.com/VenkateshL1921/Chatbot-for-mental-health-using-Llama2/assets/108605062/48ae622f-dddb-4b17-88ba-569d32463cb8)

## Result: 
![Screenshot from 2024-01-17 10-50-45](https://github.com/VenkateshL1921/Chatbot-for-mental-health-using-Llama2/assets/108605062/353d658b-1efe-46bd-8c7e-877e6a78359c)

![Screenshot from 2024-01-17 10-48-11](https://github.com/VenkateshL1921/Chatbot-for-mental-health-using-Llama2/assets/108605062/421dd07f-a1bd-45ce-bf42-b633dc77db73)



## How to run?
### STEPS:

Clone the repository

```bash
git clone https://github.com/VenkateshL1921/Chatbot-for-mental-health-using-Llama2.git
```

### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n bot python=3.8 -y
```

```bash
conda activate bot
```

### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```


### Create a `.env` and set envirnonment variables:

```ini
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
PINECONE_API_ENV = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```


### Download the quantized llama2 model & keep the model in the model directory:

```ini
# Download the Llama 2 Model:
llama-2-7b-chat.ggmlv3.q4_0.bin

# From the following link:
https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/tree/main
```

```bash
# run the following command
python store_index.py
```

```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up localhost: localhost:8080
```




