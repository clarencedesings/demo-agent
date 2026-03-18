# Shear Elegance Hair Salon Chatbot

A demo chatbot for a hair salon, powered by Ollama (phi3:mini) with a FastAPI backend and a single-page chat UI.

## Prerequisites

- Python 3
- [Ollama](https://ollama.com) running locally with the `phi3:mini` model pulled:
  ```
  ollama pull phi3:mini
  ```

## Setup

```bash
cd /home/clarence/demo-agent
pip3 install --break-system-packages -r requirements.txt
```

## Run

```bash
python3 -m uvicorn main:app --host 0.0.0.0 --port 8080
```

Open http://localhost:8080 in a browser.

## Run as a systemd service

```bash
sudo cp demo-agent.service /etc/systemd/system/
sudo systemctl daemon-reload
sudo systemctl enable --now demo-agent
```

Check status:
```bash
sudo systemctl status demo-agent
```
