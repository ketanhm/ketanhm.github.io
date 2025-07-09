---
layout: post
title:  "Running LLMs locally, without subscribing to paid plans via GUI"
date:  2024-12-25 12:20:26 -0700
categories: [Technology]
tags: [revenue growth, cost optimization]
description: How to build a ChatGPT-alternative that runs completely local and is 100% offline. 
toc: false
pin: 
comments: true
---

This blog post continues on last post. It explains how to build a ChatGPT like GUI based interface to run completely local and is 100% free of subscription plans. It also explains how to set up Open WebUI on Windows using Docker.


## What is Open WebUI 
To enable a GUI or ChatGPT-like interface, I set up Open WebUI. Open WebUI is an extensible, feature-rich, and user-friendly self-hosted AI platform designed to operate entirely offline. It supports various LLM runners like Ollama and OpenAI - compatible APIs, with built-in inference engine for RAG, making it a powerful AI deployment solution. If your computer has Nvdia GPU, it leverages CUDA acceleration. Open Web UI is primarily installed through a Docker image on Windows because Docker provides a consistent environment to run the application, isolating dependencies and simplifying deployment across different Windows systems, ensuring that the application works seamlessly regardless of the specific Windows configuration or installed libraries, minimizing compatibility issues and streamlining the setup process

Set up instructions at: [Open WebUI](https://openwebui.com)

## Examples using Open WebUI Interface

**Text classification 1:** positive, negative, or neutral sentiment

![Sentiment Analysis](https://ketanhm.github.io/images/txtclass1.png){: w="700" h="700" }

**Text classification 2:** Predefine categories News, Opinion, or Review?
Upload the article/file to chat and then prompt it to classify
![Article Analysis](https://ketanhm.github.io/images/txtclass2.png){: w="700" h="700" }

**Calling external APIs** 
```
cURL -X GET “https://api.coinbase.com/v2/currencies” | “Analyze the following API data and summarize key insights.”
```

![API Analysis](https://ketanhm.github.io/images/apicall.png){: w="700" h="700" }

It also provides sample code to use in an application

![API Analysis](https://ketanhm.github.io/images/api2.png){: w="700" h="700" }

## Coding Assistant
Enterprises are seeing tremendous improvement in software coding productivity by using LLMs. One such local-first AI coding assistant is [Continue](https://www.continue.dev). It can be set up to run inside of VS Code or Jet Brains IDE enabling:

- Chat to understand and iterate on code in the sidebar
- Autocomplete to receive inline code suggestions as you type
- Edit to modify code without leaving your current file
- Actions to establish shortcuts for common use cases

**Coding Assistant Example:** Create a blog site
At the Continue prompt in VS Code, type `Using HTML, CSS, JScript suggest setting up a blog site` and press Enter. Continue will generate code for you based on your requirements. The generated code includes HTML, CSS, JavaScript, and other set up instructions to create a blog site. You can then open the generated code in VS Code and start building your blog site. Continue also provides features such as refactoring, debugging, and testing to help you improve your coding skills. It is a powerful tool for developers who want to save time and increase their productivity by using LLMs.


![Code Generation](https://ketanhm.github.io/images/codegen.png){: w="700" h="700" }
