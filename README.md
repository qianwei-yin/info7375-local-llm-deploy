### Instructions on how to set up the models

#### Prerequisites

1. Download **ollama** app. You can find it [here](https://github.com/ollama/ollama?tab=readme-ov-file) or just click [this link for Mac](https://ollama.com/download/Ollama-darwin.zip), [this link for Windows](https://ollama.com/download/OllamaSetup.exe) and it will automatically start downloading.

2. Open the ollama app and follow the instructions on the screen.

##### Set up `Llama 3` model

1. Run `ollama run llama3` in the shell. This might take a few minutes.
2. Then you are able to prompt questions in the shell. For example, "Why is the sky blue?"
3. Also you can quit the conversation mode by typing `/bye` in the shell.
4. You can use `curl` commands to talk with the model.

   ```
   curl http://localhost:11434/api/generate -d '{
    "model": "llama3",
    "prompt":"Why is the sky blue?"
   }'
   ```

5. The response will be split into single words and send back to you using many lines of JSON.
6. If you don't like this feature, you can turn it off by using this command.

   ```
   curl http://localhost:11434/api/generate -d '{
    "model": "llama3",
    "prompt":"Why is the sky blue?",
    "stream": false # Add this line
   }'
   ```

##### Set up `Gemma` model

1. Run `ollama run gemma:2b` in the shell. This might take a few minutes.
2. The next steps are the same as above. Except one thing, you need to change `llama3` to `gemma:2b` in the curl commands.
