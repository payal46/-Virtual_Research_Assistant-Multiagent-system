
# Virtual Research Assistant

This project is a **Virtual Research Assistant** that leverages AI to fetch, summarize, and analyze research papers. It uses the **ArXiv** and **Google Scholar** databases to retrieve research papers and provides concise summaries and a detailed analysis of advantages and disadvantages. The application is built using **Streamlit** for the user interface, with AI models managed using Groq API.

## Features
- **Fetch Research Papers:** Retrieve the top 5 relevant research papers from ArXiv and Google Scholar.
- **Summarization:** Generate concise summaries of the research papers using the AI Summarizer Agent.
- **Analysis:** Provide a pointwise list of advantages and disadvantages using the AI Advantages and Disadvantages Agent.
- **Simple UI:** User-friendly Streamlit interface for easy interaction.

---

## Project Structure
```bash
Virtual-Research-Assistant/
├── agents.py           # Contains ResearchAgents class to manage AI agents
├── app.py              # Streamlit app for user interaction
├── data_loader.py      # Fetches research papers using ArXiv and Google Scholar APIs
├── .env                # Environment file to store API keys
├── requirements.txt    # List of required dependencies
├── README.md           # Documentation (This file)
```

---

## Prerequisites
- Python 3.10+
- Streamlit
- Requests
- Scholarly
- Autogen
- dotenv

### Install Dependencies
```bash
pip install -r requirements.txt
```

---

## Configuration
1. Create a `.env` file in the root directory with the following variable:
    ```bash
    GROQ_API_KEY=your_groq_api_key
    ```
2. Ensure you have a valid API key from Groq.

---

## Usage
1. **Run the Application:**
    ```bash
    streamlit run app.py
    ```
2. **Enter a Research Topic:**
    - Input your query in the search bar.
3. **View Results:**
    - The app will display the top 5 papers with a title, summary, and pros/cons analysis.
    - Each paper has a clickable link for further reading.

---

## Code Overview

### **agents.py**
- Contains the `ResearchAgents` class.
- Manages AI agents for summarization and analysis.
- Utilizes Groq API with the `deepseek-r1-distill-qwen-32b` model.

### **app.py**
- Provides a simple Streamlit-based UI.
- Fetches papers using `DataLoader`.
- Calls AI agents for summaries and analysis.
- Displays results in an organized format.

### **data_loader.py**
- Implements the `DataLoader` class.
- **fetch_arxiv_papers()** queries the ArXiv API to retrieve research papers.
- **fetch_google_scholar_papers()** uses Scholarly to fetch papers from Google Scholar.
- Includes a mechanism to suggest related topics if fewer than 5 papers are found.

---

## Potential Improvements
- Enhance UI with additional filters (e.g., date range, field of study).
- Implement error handling for API failures.
- Add authentication for API requests.
- Support additional research paper databases.

## Conclusion

The Virtual Research Assistant simplifies the research process by using AI to fetch, summarize, and analyze research papers. With Groq's LLMs, it provides concise summaries and a clear overview of advantages and disadvantages. Integrated with ArXiv and Google Scholar, the app ensures quick access to relevant academic content.

Future improvements could include support for more research platforms, enhanced model selection, and personalized recommendations. This tool is ideal for students, researchers, and professionals seeking faster insights from extensive research material.









