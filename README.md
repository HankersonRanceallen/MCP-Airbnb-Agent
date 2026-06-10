# MCP-Airbnb-Agent
# AI Airbnb Agent with MCP, vLLM, and Pydantic AI

## Overview

This project demonstrates how to build an AI-powered travel assistant using Large Language Models (LLMs), Model Context Protocol (MCP), and Pydantic AI.

The application deploys a Qwen3 model through a vLLM inference server and enhances the model with external tools through MCP servers. The agent can perform real-world actions such as retrieving the current date and time and searching Airbnb listings based on user preferences.

This project was completed as part of AMD's AI Agents learning path and focuses on modern agent development, tool calling, and LLM orchestration.

---

## Features

* Deploys a Qwen3 model using vLLM
* OpenAI-compatible API endpoint
* AI agent built with Pydantic AI
* MCP server integration
* Function/tool calling
* Real-time date and time retrieval
* Airbnb property search assistant
* Async agent execution
* Extensible architecture for additional MCP tools

---

## Technologies Used

* Python
* vLLM
* Pydantic AI
* Model Context Protocol (MCP)
* Qwen3-30B-A3B
* OpenAI-Compatible API
* AMD Instinct GPUs
* Jupyter Notebook

---

## Architecture

User Query

↓

Pydantic AI Agent

↓

Qwen3 Model (vLLM Server)

↓

MCP Servers

* Time Server
* Airbnb Server

↓

Tool Results

↓

Final Agent Response

---

## Project Workflow

### Step 1: Deploy the LLM

Launch a Qwen3 model using vLLM.

The model is served through an OpenAI-compatible endpoint and provides fast inference on AMD GPUs.

### Step 2: Create the Agent

Build a Pydantic AI agent connected to the vLLM endpoint.

The agent processes user requests and determines when tools should be used.

### Step 3: Add Custom Tools

Create a date/time tool that provides real-time information outside the model's training data.

### Step 4: Integrate MCP Servers

Replace local tools with MCP servers to provide standardized tool interfaces.

Implemented:

* Time MCP Server
* Airbnb MCP Server

### Step 5: Build a Travel Assistant

The agent can search Airbnb listings using user preferences such as:

* Destination
* Travel dates
* Number of guests
* Budget considerations

Example:

"Find a place to stay in Vancouver next weekend for 2 adults."

---

## Example Usage

### Date and Time Query

User:

What is today's date?

Agent:

Uses the MCP Time Server and returns the current date and time.

### Airbnb Search Query

User:

Find a place to stay in Vancouver for 3 nights for 2 adults.

Agent:

Uses the Airbnb MCP Server to retrieve relevant listings and provide recommendations.

---

## Skills Demonstrated

* Agent Engineering
* LLM Deployment
* MCP Integration
* Function Calling
* Tool Orchestration
* Prompt Engineering
* OpenAI-Compatible APIs
* Async Python Programming
* AI Application Development

---

## Learning Outcomes

Through this project, I learned how to:

* Deploy production-style LLM endpoints using vLLM
* Connect AI agents to external tools using MCP
* Build reasoning-and-action workflows
* Implement function calling architectures
* Develop AI assistants capable of interacting with real-world services
* Extend LLM capabilities beyond training data

---

## Future Improvements

* Weather MCP Integration
* Hotel Recommendation Scoring
* Travel Budget Planning
* Multi-Agent Collaboration
* Web Dashboard Interface
* Azure Deployment
* Containerized Deployment with Docker
