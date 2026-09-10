# Using Agentic AI on DeepSeek

To use agentic AI on DeepSeek, you need to choose an approach based on your technical comfort level: using the official **DeepSeek Harness** framework for a ready-to-use agent, or building with the **API/SDK** for custom solutions.

Below is a step-by-step process for both paths.

---

## 🛠️ Path 1: Official Framework (DeepSeek Harness)

DeepSeek offers **Harness (dsh)**, an open-source agent runtime that enables the model to use tools, read files, and execute commands.

### Step 1: Prepare Environment
Ensure Node.js is installed (version `^22.19.0` or `>=24.0.0` is recommended).

### Step 2: Deploy Harness
For a quick start, run this command in your terminal. It pulls the latest version and launches the Web UI:

```bash
npx @deepseek-ai/dsh web
```

Alternatively, you can install it globally:

```bash
npm install -g @deepseek-ai/dsh
```

### Step 3: Configure API Key
Open `http://127.0.0.1:3080` in your browser, go to **Settings → Models**, and paste your DeepSeek API Key (obtained from the official platform).

### Step 4: Set Workspace
Click **Choose workspace** to specify a folder. The agent will have read/write access to this directory for file operations.

### Step 5: Run Your Agent
Start a session and give it a task. For example:

```
Read the README.md in the current folder and summarize the project.
```

The agent will automatically reason, read the file, and return the result.

---

## 💻 Path 2: API & SDK (Custom Coding)

If you want to build a custom agent, you can use the DeepSeek API with function calling (tool calls).

### Step 1: Install SDK
Install the official OpenAI SDK (since DeepSeek's API is compatible):

```bash
pip install openai
```

### Step 2: Set Up Client
Configure the client with your API key and DeepSeek's base URL:

```python
from openai import OpenAI

client = OpenAI(
    api_key="your_api_key",
    base_url="https://api.deepseek.com"
)
```

### Step 3: Define Tools
Create a JSON schema describing the functions the agent can call (e.g., a weather lookup or database query).

### Step 4: Implement the Agent Loop
Create a loop that sends user input to the model. If the model returns `tool_calls`, execute the corresponding function in your code, append the result, and send it back to the model until it produces a final text answer.

---

## 💡 Key Considerations

- **Model Selection**: For complex planning, use **DeepSeek-R1** or **V4 Pro**. For fast tool execution, use **V3** or **Flash** models. Note that older R1 versions may have limited function calling support.
- **Security**: When using Harness, always review approval prompts before allowing the agent to write files or run shell commands, especially outside your designated workspace.
- **Stability**: Harness is in "developer preview" and may have breaking changes. Lock your version for production use.

---

If you let me know whether you plan to use the official Harness framework or build a custom API integration, I can provide more specific guidance for your use case.