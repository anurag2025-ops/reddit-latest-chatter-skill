# Reddit Latest Chatter Skill 🕵️‍♂️

**A prompt template and skill definition for AI agents to monitor real-time Reddit discussions.**

[![AI Skill](https://img.shields.io/badge/Type-AI%20Skill-blue)]()
[![Compatible with Perplexity](https://img.shields.io/badge/Tested%20On-Perplexity%20%7C%20Claude%20%7C%20GPT--4-success)]()

## 📖 What is this?
This repository contains a **skill/prompt template** designed to turn AI agents (like Perplexity, Grok, Claude, or ChatGPT) into expert open-source intelligence (OSINT) monitors. 

Instead of writing custom Python scrapers, this skill instructs the AI on how to systematically use its built-in web search and browsing tools to pull the freshest, unfiltered public sentiment on any subject directly from Reddit.

## 🚀 How to Use

> 💡 **Pro Tip for Best Results:** Because this skill relies heavily on pulling real-time, unfiltered web data, it performs best when used with AI agents built specifically for live search—such as **Perplexity** or **Grok**. Models with restricted browsing capabilities or heavy web-search latency may struggle to pull the absolute newest posts.

### Approach A: Skill-Compatible Agents (e.g., Perplexity, custom GPTs)
1. Copy the YAML contents from [`skill.yaml`](skill.yaml).
2. Add it to your agent's custom instructions, skills configuration, or system prompt.
3. Trigger it naturally: *"Use the reddit-latest-chatter skill to tell me what people are saying about the new iPhone."*

### Approach B: Manual Prompting (Claude, ChatGPT, Grok)
1. Open [`prompts/manual_prompt.md`](prompts/manual_prompt.md).
2. Copy the text and paste it into your preferred LLM to set its behavior.
3. Ask your question about recent Reddit discussions.

## ✨ Features
- **Strict Recency Filtering**: Forces the AI to ignore historical data and only pull from the last 7-14 days.
- **Structured Output**: Automatically formats output into *Themes, Sentiment Breakdown, Standout Comments,* and *Latest Posts Snapshot*.
- **Unfiltered Reality**: Explicitly instructs the AI not to sanitize or soften controversial public sentiment.

## 📂 Repository Structure
```text
.
├── README.md                 # This documentation
├── skill.yaml                # The core skill definition for agent engines
├── prompts/
│   └── manual_prompt.md      # Standalone version for standard LLM chats
└── examples/
    └── sample_output.md      # Example of what the AI generates
```

## ⚠️ Disclaimer & Best Practices
This repository provides **prompt engineering instructions** for AI models to browse public web pages. It is *not* a Python scraper or an automated bot.

If you decide to build a fully automated software implementation based on these instructions, please be aware of **Reddit's Terms of Service and their 2026 Responsible Builder Policy**. For programmatic bulk access, you must use the official Reddit API with OAuth authentication. Unauthorized bulk scraping for commercial purposes or AI training may result in IP bans or account suspension.