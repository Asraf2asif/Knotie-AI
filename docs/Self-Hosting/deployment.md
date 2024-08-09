---
title: Run The Code Locally
description: Instruction to run/deploy Knotie-AI with/without docker.
tags: Local Setup, Python, Redis, Knotie-AI
---

# 🚀 Running Code using python/conda env

If you want to run the code without Docker locally, follow these steps:

1. 🛠️ **Run Redis locally** (You can ask ChatGPT how to run Redis. Make sure to run it on port 6379). The current code uses Redis for state management (such as Conversation history etc.).

Alternatively, use the below command from knotie-ai root folder (make sure you have docker and docker-compose installed and running)
```bash
docker compose -f docker-compose-redis-only.yaml up -d
```

2. 🐍 **Install Python 3.11 and above**.

3. 🐍 **Install VirtualEnv or Anaconda**.

4. 🐍 **Create a Python environment**:
   ```bash
   conda create -n aisalesagent python=3.11
   ```

5. 🐍 **Activate the environment**:
   ```bash
   conda activate aisalesagent
   ```

6. 📥 **Download the zip or clone the repo**:
   ```bash
   git clone https://github.com/avijeett007/Knotie-AI.git
   cd knotie-ai
   ```

7. 📂 **Go inside the folder and install all the requirements**:
   ```bash
   pip install -r requirements.txt
   ```

8. 📝 **Copy `.env_sample` to `.env`**:
   ```bash
   cp .env_sample .env
   ```

9. 📝 **Open `.env` in a text editor and update all the config properties as required**.

10. 🚀 **Run the application**:
    ```bash
    python app.py

    OR

    FLASK_APP=app.py FLASK_ENV=development flask run --host=0.0.0.0 --port=5000
    ```
