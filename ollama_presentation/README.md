# Ollama basics

A minimal Python example that sends `Hello!` to a local Ollama model and prints the reply.

## Requirements

- macOS, Windows, or Linux
- Python 3.9 or newer
- Ollama installed and running on your computer
- About 1.3 GB of disk space for the `llama3.2:1b` model

This example runs locally. It does not need an account, API key, or paid plan. Model responses may be slower on computers with limited memory or no supported GPU.

## Set up and run

From this project directory, create and activate a virtual environment, install the Python package, download the model, and run the script:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
export PATH="/Applications/Ollama.app/Contents/Resources:$PATH"
ollama pull llama3.2:1b
python app.py
```

The `export PATH` line is needed on this Mac because the installer could not add Ollama to the system PATH. On another computer where `ollama` is already on PATH, omit that line. In Windows PowerShell, activate the environment with `.venv\Scripts\Activate.ps1` instead. Keep the Ollama app open while running the script so its local service is available.

The first run downloads the model. Later runs reuse the download. To try the slightly larger default `llama3.2` model, change `MODEL` in `app.py` and pull it with `ollama pull llama3.2`.

## How it works

```text
app.py ── ollama.chat(...) ──> Ollama running on this computer ──> llama3.2:1b
  <──────────────────────────── reply text ────────────────────────────────
```

## Project notes

- **Pipeline diagram:** shown above.
- **Creative piece documentation:** add a link to your video, audio, images, or screenshots here.
- **Slides:** add your public slide link here before presenting.

## References

Ollama. n.d. “Quickstart.” Accessed October 29, 2026. https://docs.ollama.com/quickstart.

Ollama. n.d. “Python Library.” Accessed October 29, 2026. https://github.com/ollama/ollama-python.
