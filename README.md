# 📊 The Analyst

**The Analyst** is an AI-powered data analysis assistant built with Streamlit. Upload a **CSV** or **PDF** file, ask questions in plain English, and get instant answers, exploratory data analysis (EDA), and interactive visualizations.

---

## ✨ Features

- 📁 **Upload CSV & PDF files** (up to 10 MB)
- 💬 **Chat-based interface**: ask questions about your data in natural language
- 🔍 **Exploratory Data Analysis (EDA)**: summary statistics, missing values, distributions, and more
- 📈 **Automatic visualizations**: bar charts, line charts, and more from a simple prompt
- 💱 **Custom currency formatting**: for example, show values in INR Crore
- 🧠 **Document Q&A**: PDF content is stored in a local vector database for retrieval
- 🧹 **Clear Chat** button to reset the conversation
- 🔐 **Secure secrets handling** using `.env`

---

## 📸 Screenshots

### Chat & Visualization
![The Analyst - Chart Output](screenshots/chart_output.png)

### Project Structure in VS Code
![Project Structure](screenshots/project_structure.png)

> 💡 Create a `screenshots/` folder in the repo and save your two screenshots there with the names above.

---

## 🛠️ Tech Stack

| Category | Tools |
|----------|-------|
| Frontend | Streamlit |
| Language | Python 3.10+ |
| Data Processing | Pandas |
| Visualization | <!-- CHANGE: Plotly / Altair / Matplotlib --> |
| LLM | <!-- CHANGE: OpenAI / Gemini / Groq / etc. --> |
| Vector Database | <!-- CHANGE: ChromaDB / FAISS --> (stored in `my_database/`) |
| Secrets | python-dotenv |

---

## 📂 Project Structure

```
29_09_2026_Proj_1/
├── .streamlit/          # Streamlit configuration
├── my_database/         # Local vector database (ignored by git)
├── app.py               # Main Streamlit app (UI & chat)
├── backend.py           # Core logic: file processing, LLM calls, retrieval
├── Visualization.py     # Chart generation logic
├── docs.py              # PDF/document handling
├── test_spill.py        # Tests
├── requirement.txt      # Python dependencies
├── .env.example         # Example environment variables
├── .gitignore
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>
```

### 2. Create and activate a virtual environment

**Windows (PowerShell):**
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

**macOS / Linux:**
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirement.txt
```

### 4. Set up environment variables

Create a `.env` file in the project root:

```env
# CHANGE: use the key name your code expects
API_KEY=your_api_key_here
```

> ⚠️ Never commit your `.env` file. It is already listed in `.gitignore`.

### 5. Run the app

```bash
streamlit run app.py
```

Open **http://localhost:8501** in your browser.

---

## 💡 How to Use

1. Upload a **CSV** or **PDF** from the sidebar.
2. Wait for the file to be processed. You'll see the current file and collection name in the sidebar.
3. Ask questions in the chat box, for example:
   - `Show me the summary statistics of this dataset`
   - `Are there any missing values?`
   - `Show total net sales by customer segment`
   - `Show the currency in INR Crore in the chart`
   - `Summarize this PDF`
4. Use **Clear Chat** to start fresh.

---

## 📋 Example Prompts

| Goal | Prompt |
|------|--------|
| EDA | "Give me an EDA report of this file" |
| Aggregation | "Total net sales by segment" |
| Visualization | "Plot monthly sales trend as a line chart" |
| Formatting | "Show values in INR Crore" |
| PDF Q&A | "What are the key points in this document?" |

---

## 🧪 Running Tests

```bash
pytest
```

---

## 🔒 Security Notes

- API keys are stored in `.env` and never pushed to GitHub.
- `.streamlit/secrets.toml` and local databases (`my_database/`) are git-ignored.
- Uploaded files are processed locally in your session.

---

## 🗺️ Roadmap

- [ ] Support for Excel (`.xlsx`) files
- [ ] Export charts and reports as PDF
- [ ] More chart types (pie, scatter, heatmap)
- [ ] Multi-file analysis
- [ ] Deployment on Streamlit Community Cloud

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m "Add your feature"`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## 👤 Author

**<Your Name>**
- GitHub: [@your-username](https://github.com/your-username)
- LinkedIn: [Your Name](https://linkedin.com/in/your-profile)

⭐ If you found this project useful, give it a star!
