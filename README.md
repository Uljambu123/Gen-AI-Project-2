# 🔎 LangChain - Chat with Search

## Project Overview
This project is a chatbot application built using LangChain and Streamlit, which integrates various search tools to enhance responses with real-time data from the web. The chatbot can retrieve information from Arxiv, Wikipedia, and DuckDuckGo, enabling it to provide enriched and relevant answers.

## Objective
The primary goal of this project is to develop an interactive chatbot that can:
- Search the web for relevant information.
- Retrieve and summarize articles from Arxiv.
- Fetch Wikipedia summaries.
- Provide accurate and real-time responses using LangChain’s agent framework.

## Key Steps in the Project
1. **Set up a Streamlit-based Chat Interface**  
   - The chatbot UI is built using Streamlit for an interactive experience.
  
2. **Integrate LangChain’s LLM and Search Tools**  
   - Uses `LangChain-Groq` for language model processing.
   - Implements `DuckDuckGoSearchRun` for real-time web search.
   - Fetches academic papers using `ArxivQueryRun`.
   - Retrieves Wikipedia summaries using `WikipediaQueryRun`.

3. **Implement an Agent Framework**  
   - Utilizes LangChain’s `initialize_agent` function with `AgentType.ZERO_SHOT_REACT_DESCRIPTION` for reasoning-based responses.
   - Handles parsing errors gracefully.

4. **Enhance User Interaction with a Chat Memory**  
   - Maintains conversation context using `st.session_state`.
   - Displays previous messages dynamically.

5. **Use a Secure API Key Mechanism**  
   - Requires users to input their Groq API key via Streamlit’s sidebar.

## Technologies Used
- **LangChain** (LLM integration, search tools)
- **Streamlit** (User interface)
- **Groq API** (Language model)
- **DuckDuckGoSearchRun** (Web search)
- **WikipediaAPIWrapper** (Wikipedia search)
- **ArxivAPIWrapper** (Academic research retrieval)
- **Python-dotenv** (Environment variable management)

## How to Run
1️⃣ Install Dependencies
Ensure you have Python installed. Then, install the required packages:
pip install -r requirements.txt

2️⃣ Set Up Environment Variables
Create a .env file in the project directory and add your Groq API key:
GROQ_API_KEY=your_api_key_here

3️⃣ Run the Application
Start the chatbot by running:
streamlit run LangChain - Chat with search_App.py

4️⃣ Interact with the Chatbot
- Enter your Groq API key in the sidebar.
- Type queries in the chat input.
- Receive responses enriched with search results.

** Future Work ** 
- Expand LLM Models: Support for additional language models like OpenAI and Hugging Face.
- Improve Search Accuracy: Fine-tune retrieval mechanisms for better query understanding.
- Add More Data Sources: Integrate sources like Google Scholar, news articles, and PDFs.
- Enhance UI/UX: Provide a more dynamic and interactive chat experience.
