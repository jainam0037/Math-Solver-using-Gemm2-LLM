# Math Solver Using Gemma2, LangChain, GROQAI, and LLMs

This project is a Streamlit-based application that allows users to chat with a SQL database and solve mathematical problems using the Groq LLM (Large Language Model) API integrated with LangChain. The agent solves mathematical questions, retrieves database information, and provides detailed explanations.

![Game Demo front page](https://github.com/user-attachments/assets/7a41768a-9c14-4e1f-b602-609f45764fb7)

## Table of Contents
- [Overview](#Overview)
- [Description](#Description)
- [Features](#features)
- [Technologies](#technologies)
- [Installation](#installation)
- [Usage](#usage)
- [Configuration](#configuration)
- [Steps for Custom Development](#steps-for-custom-development)
- [License](#license)


## Overview

This project showcases the integration of powerful tools like LangChain, Groq's Gemma2-9b LLM, and Streamlit to create an interactive mathematical problem solver and database query tool. Users can ask mathematical questions or query SQL databases in a natural language, and the system provides detailed responses by leveraging large language models (LLMs) and database agents. The project is aimed at demonstrating the power of combining natural language processing (NLP) with structured data querying.

## Description

The Math Solver project enables users to interact with a SQL database and solve complex mathematical questions by communicating with the Groq LLM through an intuitive Streamlit-based chat interface. 

Key features include:
- Solving mathematical problems using LangChain's zero-shot agents.
- Chatting with a local SQLite3 or remote MySQL database to retrieve information.
- Dynamic UI where users can switch between databases, input API keys, and interact with the system effortlessly.

By using the Groq API, the agent can break down complex questions into simple steps and present a detailed explanation in response to user queries. This makes the tool not only practical for solving equations but also for teaching concepts through detailed, logical explanations.


## Features
- Solve mathematical questions with detailed explanations.
- Integration with Groq's `Gemma2-9b` model using LangChain.
- Streamlit-based UI for interaction.
- Support for adding API keys dynamically.

## Technologies
- **Python 3.9+**
- **Streamlit** for building the web interface.
- **LangChain** for connecting with LLMs and handling database queries.
- **Groq API** for integrating the `Gemma2-9b` LLM model.

## Installation

### Prerequisites
- Python 3.9 or above.
- A Groq API Key (You can get it from [Groq API Documentation](https://groq.com/api)).

### Steps
1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/math-solver-gemma2.git
   cd math-solver-gemma2



2. Create a virtual environment and install dependencies:

bash '''

    python3 -m venv venv
    pip install -r requirements.txt
    
3. Set up your environment variables:

Create a .env file in the root directory and add your GROQ_API_KEY:

bash '''

    GROQ_API_KEY=your_groq_api_key

4. Run the Streamlit app:

bash '''

    streamlit run app.py

    
Usage
1) After starting the app, choose your database option from the sidebar:
2) Enter your Groq API Key in the sidebar if not provided in the .env file.
3) Input a mathematical question or query the database in the chat input field.
4) The agent will respond with either the result of a database query or a step-by-step solution to your mathematical question.



LLM Model Setup
The LLM model used for mathematical solving and interaction is Gemma2-9b, which is part of the Groq API. You will need an API key to access the model. This key can be provided via the sidebar or stored in the .env file as GROQ_API_KEY.

Prompt Setup
The agent uses a mathematical solver prompt designed for detailed step-by-step explanations:

bash '''

    prompt = """
    You are an agent tasked with solving users' mathematical questions. Logically arrive at the solution, and provide a detailed explanation in a step-by-step format for the question below.
    Question: {question}
    Answer:
    """

The LLM agent runs the above prompt template to provide the required answers.

Tools:
LLM: Groq Gemma2-9b model.
Wikipedia: An external tool to search for information if needed.
SQL Database: SQLite3 or MySQL to query data.



Run the code: 


![Sample question by default](https://github.com/user-attachments/assets/4e735c8f-3b87-42c8-a03e-8ca80d4aa44e)




Demo 2: 

![Demo for question](https://github.com/user-attachments/assets/acfdbaaa-1aaf-4529-aae8-197fe9f195cc)

Followup question for more clarity of its functioning

![Followup question for more clarity of its functioning](https://github.com/user-attachments/assets/8c23873f-2a8c-42ae-8384-7e3e6730e470)
