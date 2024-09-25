# ask-openai

This is a simple cli application that allows you to interact with OpenAI’s GPT models. You can send messages, receive responses, and switch between different models on-the-fly.

## Features

- Interactive Chat: Engage in a conversation with AI directly from your terminal.
- Model Selection: Dynamically switch between available GPT models using a keyboard shortcut.
- Persistent Conversation: Maintains the context of the conversation in one session for more coherent responses.

## Prerequisites

- Python 3.7+ (required by OpenAI API)
- OpenAI API Key: You need an API key from OpenAI to use their GPT models.

## Installation

1. Clone the Repository

```bash
git clone https://github.com/jZhangTk/ask-openai
cd ask-openai
```
1. Install Dependencies

Install the required Python packages using pip:

```bash
pip install -r requirements.txt
```

## Configuration

1. Configure OpenAI API Key Permissions

Go to the [API keys page](https://platform.openai.com/organization/api-keys) and make sure your OpenAI API key has

- Read permission for /v1/models
- Write permission for /v1/chat/completions

2. Set Your OpenAI API Key

Export your OpenAI API key as an environment variable:

- Linux/macOS

```bash
export OPENAI_API_KEY='your-api-key-here'
```

- Windows (Command Prompt)

```cmd
set OPENAI_API_KEY=your-api-key-here
```

- Windows (PowerShell)

```powershell
$env:OPENAI_API_KEY="your-api-key-here"
```

3. (Optional) Modify Default Settings
- Default Model: The script uses `gpt-4o-mini` by default. You can change the `model_in_use` variable to another model if desired.
- System Prompt: Modify the `system_content` variable to change the assistant’s behavior.

## Usage

Run the script:

```bash
python askOpenai
```

Or

```bash
# if running on Linux/macOS
./askOpenai
```

### Controls

- Insert a New Line: Insert a new line by pressing Enter.
- Send a Message: Type your message and press Alt-Enter.
- Change Model: Press F8 to list available models and select a different one.
- Quit: Press Ctrl-C or Ctrl-D to exit the application.

### Example Session

```
Instructions:
- Press Enter to insert a new line
- Press Alt-Enter (or Escape followed by Enter) to send a message
- Press F8 to change model
- Press Ctrl-C or Ctrl-D to quit

Ask anything.

Enter your message:
Hello, how are you?

Response:
Hello! I'm just a computer program, so I don't have feelings, but I'm here and ready to help you. How can I assist you today?
```

## Known Issues

There are some cosmetic issues related to the Change Model dialog.

- If a new line is entered before changing the model, the Change Model dialog may initially display out of alignment.
    - Moving up and down in the dialog may fix the issue.
- If you entered some text and then changed the model, the text will remain after the dialog closes. However, when you start to type again, the cursor may jump away from where it was.
    - The text you previously entered is still there. You can continue input the text where you left off.
    - If you want to see the prevously entered text, you can press Ctrl-Space and then press Left to select the text. Once you select the text, you can see it again.

## Todo

- [ ] Save and load chat history
- [ ] Add Vi input mode option
- [ ] Allow configuring the default model
- [ ] Allow configuring the default system prompt

## Contributing

Contributions are welcome! Please submit a pull request or open an issue to discuss improvements or bugs.

## License

This project is licensed under the MIT License.

## Disclaimer

This is an unofficial client and is not affiliated with OpenAI. Use it responsibly and adhere to OpenAI’s [API usage policies](https://openai.com/policies/usage-policies/).
