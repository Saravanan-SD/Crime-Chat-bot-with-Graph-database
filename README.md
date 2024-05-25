# Crime Chatbot with Graph Database

This project is a Streamlit-based chatbot application that leverages a language model and Neo4j graph database to provide responses related to crime data. The chatbot uses OpenAI's language model to understand user queries and fetches relevant data from a Neo4j database to provide context-aware answers.


![Working](https://github.com/Saravanan-SD/Crime-Chat-bot-with-Graph-database/blob/main/Screenshot%202024-05-25%20163140.png)

## Features

- User-friendly chatbot interface powered by Streamlit.
- Integration with OpenAI's language model for natural language understanding.
- Neo4j graph database for storing and querying crime data.
- Persistent session state to maintain conversation context.

## Prerequisites

- Python 3.7 or higher
- An OpenAI API key
- A Neo4j database instance

## Installation
 
1. **Clone the repository:**

    ```sh
    git clone https://github.com/Saravanan-SD/Crime-Chat-bot-with-Graph-database.git
    cd Crime-Chat-bot-with-Graph-database
    ```

2. **Install the required dependencies:**

    ```sh
    pip install -r requirements.txt
    ```

3. **Set up environment variables:**

    Create a `.env` file in the root directory of the project and add the following environment variables:

    ```ini
    OPENAI_API_KEY=your_openai_api_key
    NEO4J_URI=your_neo4j_uri
    NEO4J_USERNAME=your_neo4j_username
    NEO4J_PASSWORD=your_neo4j_password
    ```

## Usage

1. **Run the Streamlit application:**

    ```sh
    streamlit run app.py
    ```

2. **Interact with the chatbot:**

    Open your web browser and navigate to `http://localhost:8501`. You can now start interacting with the Crime Chatbot. Type your queries related to crime data, and the chatbot will provide responses based on the information stored in the Neo4j database.

## Code Overview

- **app.py**: The main application file that sets up the Streamlit interface and integrates with the language model and Neo4j database.

### Key Components

- **Environment Variables**: Loaded using `dotenv` to securely manage API keys and database credentials.
- **Neo4j Graph**: Initialized and refreshed to ensure the schema is up to date.
- **QA Chain**: Uses `GraphCypherQAChain` from LangChain and `ChatOpenAI` to process user queries and fetch relevant data.
- **Streamlit Session State**: Maintains the context of the conversation between the user and the chatbot.
