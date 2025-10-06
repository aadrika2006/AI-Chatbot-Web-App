An interactive AI-powered chatbot built with React, Node.js, TailwindCSS, and the OpenAI API.
This web app allows users to have natural conversations with an intelligent assistant in a clean, modern, and animated chat interface.

🖼️ Preview
💬 Chat Interface	⚙️ Responsive Layout
<img width="1596" height="790" alt="Screenshot 2025-10-06 160851" src="https://github.com/user-attachments/assets/22fb73f9-2c4d-4d59-b6d0-9da7de83dd28" />

<img width="1662" height="803" alt="Screenshot 2025-10-06 160904" src="https://github.com/user-attachments/assets/824e1912-3ab4-477a-8317-981bea292921" />


✨ Features

✅ Real-time AI responses powered by OpenAI GPT API

✅ Typing animation while waiting for reply

✅ Chat history persistence in localStorage

✅ Simple login / guest mode

✅ Responsive glassmorphism UI with gradients and animations

✅ Dark/Light mode toggle

✅ Voice Input (SpeechRecognition API) — optional

✅ Text-to-Speech (TTS) playback — optional


🛠️ Tech Stack Layer	Technology

💻 Frontend	React + Vite + TailwindCSS + Framer Motion

⚙️ Backend	Node.js + Express

🧠 AI	OpenAI API (gpt-3.5-turbo or Hugging Face)

🎨 Design	Glassmorphism + Gradient UI

🔊 Optional	SpeechRecognition API (voice input) + SpeechSynthesis API (TTS)

🚀 Getting Started

Follow these steps to run the project locally.

1️⃣ Clone the repository
git clone https://github.com/aadrika2006/ai-chatbot.git
cd ai-chatbot

2️⃣ Install dependencies
For frontend
cd client
npm install

For backend
cd ../server
npm install

3️⃣ Set environment variables

Create a .env file in the server/ folder and add your OpenAI API key:

OPENAI_API_KEY=your_openai_api_key_here
PORT=5000

4️⃣ Run both servers

In two terminals:

# Frontend
cd client
npm run dev

# Backend
cd server
npm start


Frontend runs at → http://localhost:5173

Backend runs at → http://localhost:5000

🗂️ Folder Structure
ai-chatbot/
├── client/ (React frontend)
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── utils/
│   │   └── App.jsx
│   ├── package.json
│   └── tailwind.config.cjs
│
└── server/ (Node.js backend)
    ├── routes/
    ├── server.js
    ├── .env
    └── package.json

🧩 How It Works

The user types or speaks a message.

The message is sent to the Node.js server via /api/chat.

The server forwards it to the OpenAI API and returns the response.

The frontend displays the AI’s reply with typing animation.

The chat history is saved in localStorage.

🔉 Optional Voice Features
🎙️ Voice Input

Enable SpeechRecognition API for hands-free chat:

const recognition = new window.SpeechRecognition();
recognition.start();
recognition.onresult = (event) => {
  const text = event.results[0][0].transcript;
  sendMessage(text);
};

🗣️ Text-to-Speech

Enable SpeechSynthesis API for the bot’s voice replies:

const speak = (text) => {
  const speech = new SpeechSynthesisUtterance(text);
  speech.lang = 'en-US';
  window.speechSynthesis.speak(speech);
};

🧑‍💻 Author

Aadrika Awasthi

🔗 LinkedIn: http://www.linkedin.com/in/aadrika-a-5690332a9

💼 GitHub: https://github.com/aadrika2006

📄 License

This project is open-sourced under the MIT License.
Feel free to use and modify it with proper attribution.

💡 Future Enhancements

✅ User accounts with Firebase Authentication

✅ Cloud DB for storing chat history

✅ Support for multiple AI models

✅ Real-time streaming responses
