# Ollama Library Tool

<img width="1088" height="774" alt="Ollama Library Tool interface" src="https://github.com/user-attachments/assets/8989ff13-9d25-4299-975d-c5042e81e20f" />

## About

Built for creators and developers working with open-source AI through [Ollama](https://ollama.com/).

Finding an AI model that suits your project and is compatible with your computer's hardware can be challenging. The **Ollama Library Tool** simplifies this process by recommending models based on your computer's capabilities and your project's requirements.

- **Ollama Library:** https://ollama.com/library — Browse Ollama's collection of available models, Note: can be confusing to navigate.
- **Ollama Library Tool:** https://browneyegirl.github.io/CART498-GenAI/A06/findyourmodel_creativepiece_1/ — Find models suited to your hardware and project.

## Running It

The interface begins with a GPU/CPU capabilities estimator to help determine which models your computer can run.

This information is then used by a TinyLlama 1.1B-powered chat interface. You can describe your project, ask questions about model compatibility, and receive recommendations from the Ollama library.

Once you've found a suitable model, simply copy the generated terminal command into your project to get started!

## Debugging 
If tinyllama won't download, make sure you have enough disk space: 
1. Inspect page then run: 
navigator.storage.estimate().then(e => console.log('free ≈', Math.round((e.quota - e.usage) / 1e6), 'MB'))
If it returns less than 1800mb, then clear disk space
2. Go to chrome settings and enable "Allow sites to save data on your device"


## Credits

Built using:
- [Ollama](https://ollama.com/)
- [TinyLlama 1.1B](https://ollama.com/library/tinyllama)
- [Kimi K3](https://ollama.com/)
