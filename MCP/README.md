# 🌐 MCP Server Explained

### A Beginner-Friendly Guide to Model Context Protocol

![MCP Banner](https://img.shields.io/badge/MCP-Model%20Context%20Protocol-blueviolet?style=for-the-badge)
![AI](https://img.shields.io/badge/AI-LLM%20Tools-ff69b4?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Learning%20Notes-success?style=for-the-badge)

---

## 📌 Overview

This repository contains beginner-friendly notes on **MCP Server**, also known as **Model Context Protocol**.

MCP helps AI models connect with external tools, resources, and real-world systems in a structured way.

In simple words:

> **LLMs can generate answers, but MCP gives them tools and context to take useful actions.**

---

## 🤖 What is an LLM?

**LLM stands for Large Language Model.**

An LLM is basically a smart text-completion software that predicts the next word or response based on the data it has learned from books, websites, code, articles, and other sources.

Popular examples of LLMs:

* ChatGPT
* Claude
* Gemini
* LLaMA
* Mistral

---

## ✨ What Can an LLM Do?

An LLM can understand and generate text.

It can:

* ✍️ Write essays
* 📧 Draft emails
* 🧑‍💻 Write code
* 🗄️ Generate database queries
* 📚 Explain concepts
* 📝 Create documentation
* 🔍 Summarize content
* 💡 Suggest solutions

---

## ⚠️ What Can an LLM Not Do Directly?

An LLM cannot perform real-world actions by itself unless it is connected to tools.

For example:

| LLM Can Do             | LLM Cannot Do Directly        |
| ---------------------- | ----------------------------- |
| Write an email         | Send that email               |
| Write a database query | Run that query on a database  |
| Suggest code changes   | Edit project files            |
| Explain an error       | Read live console logs        |
| Write a search query   | Search the internet by itself |

So basically:

> **LLM thinks and writes. Tools help it take action.**

---

## 🛠️ Why Do We Need Tools?

Tools allow AI models to perform actions beyond text generation.

Examples of tools:

* 🌍 Internet search tool
* 📁 File reading tool
* ✏️ File editing tool
* 🧑‍💻 GitHub issue fetching tool
* 💬 Slack message reading tool
* 🗄️ Database query tool
* 📧 Email sending tool
* 🧪 Code testing tool

Without tools, an LLM can only give suggestions.
With tools, it can actually interact with real systems.

---

## 🔗 What is MCP?

**MCP stands for Model Context Protocol.**

It is a standard protocol designed by **Anthropic** that allows AI models to connect with tools, data sources, and services in a structured way.

In simple words:

> **MCP is a bridge between AI models and real-world tools.**

---

## 🚀 Why is MCP Important?

Different AI models are good at different tasks.

For example:

* Claude may be good at reasoning.
* GPT may be good at writing and documentation.
* Gemini may be useful for multimodal or testing tasks.
* Some models may perform better at coding.
* Some models may perform better at analysis.

But the real power comes when these models can access the right tools and context.

MCP helps by creating a common communication standard between:

* AI models
* Clients
* Tools
* Resources
* External systems

---

## 🧠 Importance of Context in LLMs

Context is one of the most important things for any LLM.

The same word can have different meanings depending on the context.

Example:

```text
fan
```

This can mean:

* A ceiling fan
* A fan of an artist
* A cooling fan in a computer

But if we say:

```text
The fan in my room is not working.
```

Now the model understands that we are talking about a ceiling fan.

That is why:

> **The better the context, the better the AI response.**

MCP helps provide better context by connecting AI models with useful external data.

---

## 💻 What is a Client in MCP?

A client is the application that talks to the MCP server.

Examples of clients:

* Cursor
* Claude Desktop
* AI coding assistants
* IDE-based AI tools
* Custom AI applications

The client sends requests to the MCP server and receives tools, resources, or context in return.

Example:

```text
User → Cursor → MCP Server → Tools / Resources
```

---

## 🖥️ What is an MCP Server?

An MCP server is a separate server that provides tools and resources to the AI model.

Each MCP server is usually designed for a specific purpose.

Examples:

### 🧑‍💻 GitHub MCP Server

Provides access to:

* Repository issues
* Pull requests
* Commits
* Discussions
* Code files

### 💬 Slack MCP Server

Provides access to:

* Slack channels
* Team discussions
* Error reports
* Internal messages

### 📁 File System MCP Server

Provides access to:

* Read files
* Write files
* Edit files
* Create folders
* Understand project structure

---

## 🔄 Simple MCP Flow

Suppose the user asks:

```text
Check if the error I am getting in this repo is already mentioned in any GitHub issue or discussed in Slack.
```

To answer this properly, the AI needs two types of context.

---

### 1. GitHub Context

The AI needs access to GitHub issues.

So it asks the GitHub MCP server:

```text
Give me the latest list of issues from this repository.
```

The GitHub MCP server returns fresh issue data.

---

### 2. Slack Context

The AI also needs access to Slack messages.

So it asks the Slack MCP server:

```text
Check if this error was discussed in any Slack channel.
```

The Slack MCP server returns relevant Slack messages.

---

### Final Result

Now the AI has both contexts:

* GitHub issues
* Slack discussions

Then it can compare the error and give a meaningful answer.

---

## 🧩 Important MCP Concepts

MCP mainly includes the following concepts:

---

## 🛠️ 1. Tools

Tools are functions that perform actions.

Examples:

```text
read_file
write_file
search_internet
run_database_query
fetch_github_issues
read_slack_messages
send_email
```

A tool is basically a function that helps the AI do real work.

Example:

```text
Tool: read_file
Action: Reads content from a file
```

```text
Tool: search_github_issues
Action: Searches issues inside a GitHub repository
```

---

## 📁 2. Resources

Resources are data or attachments provided to the LLM.

Examples:

* CSV files
* PDFs
* Documents
* Code files
* API docs
* Error logs
* Project files

Resources help the AI understand the background information.

Example:

```text
Here is a CSV file. Analyze the sales data.
```

Here, the CSV file is a resource.

---

## 📝 3. Prompts

Prompts are reusable templates for clients.

They help standardize instructions and improve AI responses.

Example:

```text
You are a senior software engineer. Review this code and suggest improvements.
```

Prompts can help with:

* Improving user instructions
* Making vague prompts more detailed
* Standardizing workflows
* Saving time
* Making AI responses more accurate

---

## 🔁 4. Sampling

Sampling is a way to query or use other models.

For example, suppose you are using Claude, but you want:

* Gemini to create testing files
* GPT to write the README file
* Claude to review the architecture

This allows different models to be used for different tasks.

Example:

```text
Claude → Code reasoning
Gemini → Test generation
GPT → Documentation writing
```

---

## 🔌 Client and MCP Server Communication

In MCP, the client communicates with the MCP server.

There are mainly two communication methods:

---

### 1. Server-Sent Events

Server-Sent Events allow the server to continuously send updates to the client.

This is useful for:

* Streaming updates
* Real-time communication
* Long-running tasks
* Continuous status updates

---

### 2. Message Endpoint

A message endpoint is used when the client sends a request and receives a response.

Example:

```text
Client → MCP Server: Read this file
MCP Server → Client: Here is the file content
```

---

## 🏗️ MCP Architecture

```text
User
 ↓
Client
 ↓
MCP Server
 ↓
Tools / Resources / External Services
```

Example:

```text
User asks a question
 ↓
Cursor receives the request
 ↓
Cursor talks to MCP Server
 ↓
MCP Server uses GitHub / Slack / File tools
 ↓
Context is returned to the AI model
 ↓
AI gives a better answer
```

---

## 🌟 Real-Life Example

User prompt:

```text
Fix the bug in my project and check if this error is already discussed in GitHub issues.
```

To solve this, the AI needs:

* 📁 Project file access
* ⚠️ Console error access
* 🧑‍💻 GitHub issue access
* ✏️ Code editing tool
* 🧠 Proper project context

MCP servers provide all these tools in a structured way.

---

## 📊 LLM vs LLM with MCP

| Feature              | LLM Only | LLM with MCP |
| -------------------- | -------- | ------------ |
| Generate text        | ✅        | ✅            |
| Write code           | ✅        | ✅            |
| Access project files | ❌        | ✅            |
| Search GitHub issues | ❌        | ✅            |
| Read Slack messages  | ❌        | ✅            |
| Edit files           | ❌        | ✅            |
| Use external tools   | ❌        | ✅            |
| Take real actions    | ❌        | ✅            |

---

## 🎯 One-Line Summary

> **LLMs generate answers, but MCP gives them tools, context, and access to take useful actions.**

---

## 🧠 Final Definition

MCP is a protocol that helps AI models connect with tools, resources, and external systems.

It allows AI assistants to move from just answering questions to actually understanding context and performing actions.

---

## 🏁 Conclusion

MCP is important because modern AI assistants are no longer limited to only generating text.

With MCP, AI can:

* Understand your project
* Read files
* Search issues
* Access tools
* Use resources
* Communicate with external systems
* Help with real-world workflows

That is why MCP is becoming an important part of agentic AI systems.

---

## ⭐ Key Takeaway

```text
Without MCP:
AI can only suggest.

With MCP:
AI can understand, connect, and act.
```

---

## 🙌 Author

Made with ❤️ by **Sonal Mittal**

---
