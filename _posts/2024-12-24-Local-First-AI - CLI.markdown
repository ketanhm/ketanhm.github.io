---
layout: post
title:  "Running LLMs locally, without subscribing to paid plans using CLI"
date:  2024-12-24 12:20:26 -0700
categories: [Technology]
tags: [revenue growth, cost optimization]
description: How to build a ChatGPT-alternative that runs completely local and is 100% offline. 
toc: false
pin: 
comments: true
---

Running LLMs (that are open weights or open source) on local/on-premise computer has few benefits:

- **Data Privacy and security**: private data remains on your device, as it doesn’t need sending data over the internet to the cloud
- **Offline Capability**: Once downloaded, models can run without the internet
- **No paid subscriptions**: Computer and inference is on your machine hence no additional cost for your application (important for token-intensive applications)
- **Speed Increase**:  Depending on your desk/laptop hardware(slower inference, without GPU/NPU), you may see potential speed increase due to no HTTP call overheads
- **Customization**: Local deployment allows custom modifications to models

There are many open-source tools for hosting open weights LLMs locally for inference - command line interface (CLI) or full GUI based. 

Few popular are GPT4ALL, Jan.ai, Ollama. 

It is easy to set up local-first AI, running open-source FMs directly on your computer.

On a windows laptop, I chose Ollama and Open WebUI as runners for LLMs.

## What is Ollama?
It’s an open-source tool and one of the most active inference server in the open source community. It allows you to run LLMs or SLMs on your local machine, and is optimized for both CPU’s and GPU’s. One can use it to download foundation models directly, and it provides a library of quantized models, which are optimized versions of the models at the cost of some quality loss. That means that you can choose your trade off between speed and quality depending of your needs. It comes with an OpenAI-compatible API, so it can works with many existing applications, and it makes it easy to swap in the model you’re using when working locally or deploying to production.

Ollama runs as a native Windows application (wsl not needed), and has support for NVIDIA and AMD Radeon GPU.

Set up instructions at: [Ollama](https://www.ollama.com)

List of models available for download on [Models Library](https://www.ollama.com/library)

[1/25/2025 update], Deepseek-r1 is among the most popular with 1.4MN+ pulls



Once Ollama is installed, it is very easy to run from either Windows command-line shells: 
Command shell or PowerShell 

## Basic Ollama commands and output:

![Ollama Commands](https://ketanhm.github.io/images/ollama-commands.png){: w="700" h="400" }

## Examples using Command Line Interface (CLI)

**Text Summarization 1** summarizing a large text file e.g. monopoly.txt

![Summarization](https://ketanhm.github.io/images/txtgen1.png){: w="700" h="700" }


Note: The ‘<’ operator didn’t work in Powershell, but works on command shell


**Text Summarization 2**  summarize Git User Manual (4K lines long)
Download user manual here [Git User Manual](https://github.com/git/git/blob/master/Documentation/user-manual.txt)

![Summarization](https://ketanhm.github.io/images/txtgen2.png){: w="700" h="700" }


**Content Creation:** Write an article, or blog post, or create copy


![content creation](https://ketanhm.github.io/images/create-content.png){: w="700" h="700" }


![Create Blog](https://ketanhm.github.io/images/blogtxt.png){: w="700" h="700" }

**Answering Questions:** Ask question and let Gen AI offer recommendation

![Question & Recommendation](https://ketanhm.github.io/images/question-recommendation.png){: w="700" h="700" }

