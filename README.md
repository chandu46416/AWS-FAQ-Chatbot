# AWS FAQ Chatbot

Welcome to the AWS FAQ Chatbot! This is a simple chatbot designed to answer questions related to AWS. It utilizes the TF-IDF vectorization technique and cosine similarity to find and provide the most relevant answers from a pre-existing dataset of questions and answers.

## Table of Contents

- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [How It Works](#how-it-works)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The AWS FAQ Chatbot uses machine learning to respond to user queries about AWS. It leverages a dataset of frequently asked questions and their answers, transforming them into TF-IDF vectors and computing cosine similarity to find the best match for user queries.

## Installation

1. **Clone the Repository:**
    ```bash
    git clone https://github.com/yourusername/AWS_FAQ_Chatbot.git
    cd AWS_FAQ_Chatbot
    ```

2. **Create and Activate Virtual Environment (Optional but recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Run the Chatbot:**
    ```bash
    python chatbot.py
    ```

2. **Interact with the Chatbot:**
    - The chatbot will greet you and prompt you to ask any AWS-related questions.
    - Type your question and press Enter to get a response.
    - Type `stop` and press Enter to exit the chatbot.

## Dataset

The dataset used for this chatbot is `AWS_FAQ_Bot.csv`, which contains a collection of frequently asked questions about AWS and their corresponding answers. Ensure this file is in the same directory as the `chatbot.py` script.

## How It Works

1. **Data Loading and Preprocessing:**
    - The dataset is loaded using pandas.
    - Missing values are dropped to ensure data quality.

2. **TF-IDF Vectorization:**
    - Both questions and answers are transformed into TF-IDF vectors using `TfidfVectorizer` from `sklearn`.

3. **Cosine Similarity:**
    - For each user query, the chatbot computes the cosine similarity between the query vector and the question vectors in the dataset.
    - The chatbot selects the answer corresponding to the most similar question vector.

4. **Response Generation:**
    - The chatbot prints the answer to the user.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes. Ensure your changes are well-documented and tested.

Feel free to reach out if you have any questions or need further assistance. Enjoy using the AWS FAQ Chatbot!
