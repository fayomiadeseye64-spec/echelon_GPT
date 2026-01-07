**🤖 Echelon GPT (Clever ChatGPT)**

Echelon GPT is a lightweight Streamlit-based AI chat application powered by LangChain and OpenAI.
It allows users to interact with a GPT model through a simple web interface by securely providing their OpenAI API key.

✨ Features

🧠 GPT-powered conversational AI

🌐 Simple and clean Streamlit UI

🔐 Secure OpenAI API key input (password-protected)

🎈 Interactive UI elements (sidebar, balloons, placeholders)

🖼️ AI-themed interface with image support

🛠️ Tech Stack

**Python

Streamlit**

LangChain (Community)

**OpenAI API**

**📁 Project Structure
echelon_GPT/**
│
├── app.py               # Main Streamlit application
├── requirements.txt     # Python dependencies
├── ai.png               # UI image asset
└── README.md            # Project documentation

**🚀 Installation & Setup**
1️⃣ Clone the repository
git clone https://github.com/fayomiadeseye64-spec/echelon_GPT.git
cd echelon_GPT

2️⃣ Create & activate a virtual environment (recommended)
python -m venv venv


Linux / macOS

source venv/bin/activate


Windows

venv\Scripts\activate

3️⃣ Install dependencies
pip install -r requirements.txt

▶️ Running the Application

Start the Streamlit app with:

streamlit run app.py


Once running, open your browser at:

http://localhost:8501

🔑 OpenAI API Key

Enter your OpenAI API key in the sidebar.

The app validates the key (must start with sk-).

Your key is not stored.

🧪 How It Works

User enters a prompt in the text area

The app sends the request via LangChain

OpenAI generates a response

The response is displayed in real-time

🖼️ UI Preview

The app includes:

Sidebar with API key input

AI image (ai.png)

Dynamic placeholder text

Interactive animations (balloons 🎈)

⚠️ Notes

You must have an active OpenAI API key

Internet connection required

Intended for learning, demos, and prototypes

📜 License

This project is open-source.
You may add a license such as MIT if you plan to share publicly.

👤 Author

Fayomi Adeseye
🔗 GitHub: https://github.com/fayomiadeseye64-spec

✅ This README is fully aligned with your code
If you want next:

a professional badge section

deployment guide (EC2 / Streamlit Cloud)

or README with screenshots

Just say the word 🚀
