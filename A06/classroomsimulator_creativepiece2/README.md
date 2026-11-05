# Ollama Classroom Simulation

A small first-person classroom simulation built in Unity, where the player can walk around, approach a teacher, and ask questions through a chat box. The project explores how a locally running language model can give a game character responses beyond a fixed dialogue script.

## Demo video

<video controls width="800">
  <source src="./classroomsimulator_creativepiece2.mov" type="video/mp4">
  Your browser does not support the video tag.
</video>

## Program Download 
https://github.com/maiaarrais/OllamaPresentation


## What happens in the classroom?

The room contains a teacher, Ms. Rivera, and students sitting at desks. The player moves through the classroom in first person and presses **E** near the teacher while facing her to start a conversation. Movement pauses so the player can type a question and read her answer.

The teacher turns toward the player and makes small head, arm, and hand movements when an answer arrives. These are procedural animations controlled by Unity code. Ollama generates the dialogue text. The gestures are timed approximately to the answer’s length, rather than synchronized to individual words.

## How Ollama is connected

Unity sends the player’s question to Ollama’s local chat API:

```text
http://localhost:11434/api/chat
```

The request includes the teacher’s instructions, the recent conversation, and the new question. This demo uses **`llama3.2:3b`**, which runs on the same computer as the Unity program. Ollama returns a generated answer, and Unity displays it in the dialogue box.

The script keeps the last six completed question-and-answer exchanges as context. **Start over** clears that conversation history. The model is not being trained during play: its behavior is guided by the instructions and context sent with each request.

## Running the project

1. Install [Ollama](https://ollama.com/) and keep the application running.
2. Download the model in Terminal:

   ```bash
   ollama pull llama3.2:3b
   ```

3. Open the Unity project folder (`My project`) through Unity Hub, using the Editor version recorded in `ProjectSettings/ProjectVersion.txt`.
4. Open the saved classroom scene. On the teacher’s **Ollama Teacher** component, check that **Model** is `llama3.2:3b` and **Endpoint** is `http://localhost:11434/api/chat`.
5. Press **Play** and click inside the Game view.

| Control | Action |
| --- | --- |
| WASD | Walk |
| Mouse | Look around |
| E | Talk to the nearby teacher while facing her |
| Send | Submit a typed question |
| Escape | Close the conversation and resume walking |
| Start over | Clear the conversation history |

## Changing the teacher

Edit **Teacher Instructions** in the Unity Inspector to change her subject, personality, or response style. Stop Play mode before editing and save the scene to keep the changes. Start a fresh conversation when testing a different set of instructions.

## Notes

Once the model is downloaded, local dialogue can run without an internet connection or a Unity AI subscription. Response speed depends on the computer, and the first response may take longer while the model loads.

Answers can be inaccurate; the teacher is an experimental game character, not a verified educational resource.

The Unity scripts and scene setup were developed with ChatGPT assistance.

