# Google Gemini (2.5 Flash Model) Integration

This project demonstrates how to integrate the Google Gemini (2.4 Flash Model) using the Google Vertex AI API. It includes setting up authentication, making predictions, and securely managing API keys.

---

## 🚀 Features
- Text generation using the 2.4 Flash Model (`text-bison-002`)
- Secure handling of API keys with `.env`
- Example for both Service Account and API Key authentication
- Supports custom parameters like `max_output_tokens`, `temperature`, `top_p`, and `top_k`

---

## 📂 Project Structure
```
.
├── .env                 # Environment variables
├── main.py              # Code to interact with the Gemini model
├── requirements.txt     # Python dependencies
└── README.md            # Project documentation
```

---

## 🛠️ Setup Instructions

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/google-gemini-integration.git
cd google-gemini-integration
```

### 2. Create a Virtual Environment
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure the `.env` File
Create a `.env` file and add the following:
```plaintext
GOOGLE_APPLICATION_CREDENTIALS="path/to/your-service-account-file.json"
PROJECT_ID="your-google-cloud-project-id"
LOCATION="us-central1"
```

### 5. Run the Project
```bash
python main.py
```

---

## 🧬 Example Usage
Example request to generate a joke using the 2.4 Flash Model:
```python
response = model.predict(
    "Tell me a joke about programming!",
    max_output_tokens=100,
    temperature=0.7,
    top_p=0.8,
    top_k=40,
)
print(response.text)
```

---

## 🛡️ Security Best Practices
- **NEVER** commit your `.env` file to GitHub. Add it to `.gitignore`.
- Use service accounts with the least privilege principle.

---

## 🔗 Useful Links
- [Google Vertex AI Documentation](https://cloud.google.com/vertex-ai)
- [python-dotenv Documentation](https://pypi.org/project/python-dotenv/)

---

## 📜 License
This project is licensed under the MIT License.

---

## 👤 Author
[Adwin T Sunil](https://github.com/yourusername)

