# 🗞️ CrewAI – Local News Digest AI Agents

A modular AI system that collects, summarizes, and categorizes local news using OpenAI-powered agents. Ideal for keeping users informed with short, relevant, location-specific news digests.


## 📌 Project Overview

**CrewAI** leverages a crew of intelligent agents to automate the process of digesting local news:

- 🔍 **Collector** – Gathers local news from RSS feeds or custom sources  
- 🧠 **Summarizer** – Condenses each article using OpenAI’s Chat API  
- 🗂️ **Classifier** – Tags articles under topics like Politics, Weather, Community  
- 🧾 **Aggregator** – Compiles the summaries into a structured digest  
- ✉️ **Notifier** – Delivers the digest via CLI, JSON, or future email integration



## 🚀 Getting Started

### 1. Clone the Repository



2. Install Dependencies
For Python:


pip install -r requirements.txt
(If using Node.js, use npm install instead.)

3. Set Up Your Environment
Create a .env file in the root directory:


OPENAI_API_KEY=sk-1234ABCD5678EFGH9012IJKL3456MNOPQRSTUVWX
ℹ️ Important: Never share your real API key. This key is a placeholder for demonstration only.

🧠 How It Works
mermaid

flowchart LR
    A[User Input: Location] --> B[Collector]
    B --> C[Summarizer (OpenAI)]
    C --> D[Classifier]
    D --> E[Aggregator]
    E --> F[Notifier (CLI/Email/JSON)]
Each component acts independently, making it easy to upgrade or replace one without breaking the whole system.

🧪 Example Run

python crew_digest.py
User Input:


Enter your city or region: Mumbai
Sample Output:

📰 Daily Digest – Mumbai

🏛️ Politics:
- Civic body announces new metro rail phase...

🌦️ Weather:
- Monsoon expected to intensify midweek...

🎭 Community:
- Kala Ghoda festival dates announced...

Total articles processed: 18
📂 Project Structure
arduino

crewai/
├── agents/
│   ├── collector.py
│   ├── summarizer.py
│   ├── classifier.py
│   └── aggregator.py
├── crew_digest.py
├── config/
│   └── sources.yaml
├── .env
├── requirements.txt
└── README.md
🔧 Features
✅ Location-based news gathering

✅ Summarization via OpenAI API

✅ Categorization by topic

✅ Extensible architecture (easily plug in APIs or add delivery modes)

📈 Roadmap
 Email delivery system via SMTP or SendGrid

 Add local language support

 Web dashboard interface

 Scheduled digests using cron or background tasks

📘 Tech Stack
Python 3.12

OpenAI GPT-4 (via openai Python SDK)

Requests, feedparser, dotenv, rich

Modular agent architecture

✅ Best Practices
Never commit your .env or actual API keys

Respect news sites' robots.txt policies if scraping

Limit API usage to avoid quota overages

📄 License
This project is licensed under the MIT License.

🙌 Credits
Made with ❤️ by @pratyakshcodeclash
Inspired by OpenAI Agent architecture and modern news summarization tools






