# MCP - OpenAI implementation through OpenAI apps and local MCP

## Prerequisites

- Npm
- Ngrok
- Working ChatGPT account
  

## Installation

1. **Navigate to the project directory:**
   ```bash
   cd mcp-openai
   ```
   
2. **Install Node MCP SDK**
   ```bash
   npm install @modelcontextprotocol/sdk @modelcontextprotocol/ext-apps zod
   ```
3. **Run the server**
   ```bash
   node server.js
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
