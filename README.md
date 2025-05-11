## Gen AI project - Chat with SQL DB with Langchain SQLTookit and Agent

### Objective:

The app enables users to "chat" with a SQL database (either SQLite or MySQL) by asking questions in natural language. The system interprets the queries, retrieves the relevant data, and provides answers in a conversational manner.

### Key Features:

1. Database Connectivity: Users can choose between a local SQLite database (student.db) or connect to a MySQL database by providing credentials (host, user, password, and database name).

2. LangChain SQL Agent: The app uses LangChain's SQLDatabaseToolkit and create_sql_agent to create an AI agent capable of understanding and executing SQL queries based on user input.

3. Groq API Integration: The app leverages the Groq API (with the Llama3-8b-8192 model) as the underlying language model to process natural language queries and generate SQL queries.

4. Streamlit Interface: The app provides an interactive chat interface where users can ask questions, and the agent responds with data fetched from the database. The agent's thought      process is displayed in real-time using StreamlitCallbackHandler.

### Workflow:

* Users select the database type (SQLite or MySQL) and provide necessary credentials.

* The app connects to the database using SQLAlchemy and configures the LangChain SQL toolkit.

* Users input natural language queries (e.g., "Show me all students with grades above 90").

* The LangChain agent interprets the query, generates and executes the corresponding SQL query, and returns the results in a conversational format.

### Technical Highlights:

* Dynamic Database Connection: The app dynamically connects to either SQLite or MySQL based on user input.

* Caching: Database connections are cached for efficiency using st.cache_resource.

* Error Handling: The app ensures all required MySQL credentials are provided before attempting a connection.

* Conversation History: The chat history is maintained in st.session_state, allowing users to continue conversations seamlessly.

### Use Case:

This tool is ideal for non-technical users who need to query databases without writing SQL. It can be used in educational settings, business analytics, or any scenario where database interaction is required.

* In summary, this project demonstrates the integration of LangChain, Streamlit, and Groq API to create a user-friendly, AI-powered interface for querying SQL databases using natural language. It showcases my ability to build practical, interactive GenAI applications with robust backend functionality.