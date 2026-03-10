# MCP - OpenAI Apps and Local MCP

## What it does?

This is a working code to demonstrate MCP integration with OpenAI ChatGPT. The integration allows **Creation of Tasks**, and **Completion of Tasks** through prompts. The MCP server is created on local machine using Node MCP SDK.

The code is for testing use only, to quickly setup and understand MCP integration.


## Prerequisites

- Npm
- Ngrok
- Working ChatGPT account
  

## Installation

1. **Navigate to the project directory:**
   ```bash
   cd ai-mcp-openai-ts
   ```
   
2. **Install Node MCP SDK**
   ```bash
   npm install @modelcontextprotocol/sdk @modelcontextprotocol/ext-apps zod
   ```
3. **Run the server**
   ```bash
   npx run dev
   ```

4. **Expose local port to public internet**
   ```bash
   ngrok http 8787
   ```

5. **ChatGPT account changes**
   - Enable "Developer Mode" in ChatGPT through "Settings -> Apps -> Advanced Settings"
   - Click "Create app". Provide Name, MCP Server URL (http://<ngrok url from step 4>:8787/mcp)
   - Choose "No Auth" and tick "I understand..." for the test. Click "Create"

6. **ChatGPT test**
   - Go to "New chat"
   - Click "+" -> "...More" and Choose the app created in Step 5
   - Type prompt "Add a new task to read book on MCP integration". You should see a UI with task created
   - Type prompt "Complete task to read book on MCP integration". You should see a UI with task ticked and strikethrough


## Screenshots

**Task Creation**

<img width="1017" height="610" alt="Task Created" src="https://github.com/user-attachments/assets/680a73f2-95a2-4dc4-bac8-905b96acbb75" />



**Task Completion**

<img width="1017" height="610" alt="Task Completed" src="https://github.com/user-attachments/assets/701cb112-c8bf-48d6-b478-3ded532a18b5" />

