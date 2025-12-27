# Text-to-SQL Chatbot (LLM-Powered)

An intelligent chatbot that converts natural language questions into SQL queries and retrieves answers from your database. Supports both SQLite and MySQL databases.


## Features

- 💬 **Natural Language to SQL**: Ask questions in plain English
- 🗄️ **Multi-Database Support**: Works with SQLite and MySQL
- 🤖 **AI-Powered Agent**: Autonomous query generation and execution
- 📊 **Real-time Results**: Instant database insights
- 🔄 **Streaming Responses**: Live agent thought process
- 🔒 **Secure Connections**: Password-protected database credentials

## Tech Stack

- **Frontend**: Streamlit
- **LLM**: Groq (Llama 3-8B)
- **Agent Framework**: LangChain SQL Agent
- **Databases**: SQLite3, MySQL
- **ORM**: SQLAlchemy

## Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/text-to-sql-chatbot.git
cd text-to-sql-chatbot
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Set up the sample database (optional):
```bash
python sqlite.py
```

4. Run the application:
```bash
streamlit run app.py
```

## Usage

### Option 1: Use Sample SQLite Database
1. Select "Use SQLLite 3 Database- Student.db"
2. Enter your Groq API key
3. Start asking questions about student data

### Option 2: Connect to MySQL
1. Select "Connect to your MySQL Database"
2. Provide MySQL connection details:
   - Host
   - Username
   - Password
   - Database name
3. Enter your Groq API key
4. Query your MySQL database in natural language

## Example Queries

- "How many students are in the database?"
- "Show me all students in Data Science class"
- "What is the average marks of students in section A?"
- "List students with marks above 80"
- "Who scored the highest marks?"

## Database Schema (Sample)

The included `student.db` contains:

| Column  | Type        |
|---------|-------------|
| NAME    | VARCHAR(25) |
| CLASS   | VARCHAR(25) |
| SECTION | VARCHAR(25) |
| MARKS   | INT         |

## Requirements
```
streamlit
langchain
langchain-groq
langchain-community
sqlalchemy
mysql-connector-python
python-dotenv
```

## Project Structure
```
├── app.py           # Main Streamlit application
├── sqlite.py        # SQLite database setup script
├── student.db       # Sample SQLite database
└── requirements.txt # Project dependencies
```

## Configuration

- **Model**: Llama3-8b-8192
- **Agent Type**: Zero-shot ReAct Description
- **Streaming**: Enabled
- **Cache TTL**: 2 hours

## Security Notes

- Database connections are read-only for SQLite
- MySQL credentials are password-protected in the UI
- API keys are not stored persistently

## License

MIT License

## Author

**Tanvir Ahammed**  
📧 tanvir7535@gmail.com

Built with ❤️ using Streamlit, LangChain, and Groq
