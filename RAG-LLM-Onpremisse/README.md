
# RAG Agentic Pattern

## Resumo
As técnicas de **geração aumentada por recuperação** melhoram a atualizabilidade do conhecimento dos agentes para a realização de objetivos e mantêm a privacidade dos dados em implementações de agentes/sistemas baseados em modelos fundamentais locais.

## Contexto
Agentes baseados em grandes modelos fundamentais não estão equipados com conhecimento relacionado a domínios específicos, especialmente em dados locais altamente confidenciais e sensíveis à privacidade, a menos que sejam ajustados ou pré-treinados com dados de domínio.

## Problema
Dada uma tarefa, como os agentes podem conduzir o raciocínio com dados/conhecimentos que não foram aprendidos pelos modelos fundamentais durante o treinamento do modelo?

## Forças
- **Falta de conhecimento**: O processo de raciocínio pode ser pouco confiável quando o agente é solicitado a realizar tarefas específicas de domínio que não estão em seu reservatório de conhecimento.
- **Sobrecarga**: O ajuste fino de grandes modelos fundamentais usando dados locais ou o treinamento de um grande modelo fundamental localmente consome muitos recursos computacionais e custos.
- **Privacidade dos dados**: Os dados locais são confidenciais e não podem ser usados para treinar ou ajustar modelos.

## Solução
A ![Figura 6](link-da-imagem) ilustra uma representação gráfica de alto nível da geração aumentada por recuperação. RAG é uma técnica para melhorar a precisão e a confiabilidade dos agentes com fatos recuperados de outras fontes (dados internos ou online). As lacunas de conhecimento onde os agentes estão faltando em memória são preenchidas usando o conhecimento parametrizado gerado em bancos de dados vetoriais. Por exemplo, durante a geração de planos, passos específicos podem exigir informações que não estão na memória original do agente. O agente pode recuperar informações do conhecimento parametrizado e usá-las para o planejamento, enquanto a resposta aumentada (ou seja, o plano) é retornada ao usuário. O processo de recuperação não requer pré-treinamento ou ajuste fino do modelo servido pelo agente, preservando a privacidade dos dados locais, reduzindo custos de treinamento e computação e fornecendo informações mais precisas e atualizadas. Os dados locais recuperados podem ser enviados de volta ao agente via prompts (considerando o tamanho da janela de contexto), enquanto o agente é capaz de processar as informações e gerar planos por meio de aprendizado contextual. Atualmente, existe um conjunto de técnicas RAG focando em vários aspectos de aprimoramento, fontes de dados e aplicações, como RAG federado e RAG baseado em grafo.

## Consequências

### Benefícios
- **Recuperação de conhecimento**: Os agentes podem buscar e recuperar conhecimento relacionado às tarefas dadas, garantindo a confiabilidade dos passos de raciocínio.
- **Atualizabilidade**: Os prompts/respostas gerados usando RAG pelo agente em dados internos ou online são atualizáveis pelo conhecimento parametrizado complementar.
- **Privacidade dos dados**: O agente pode recuperar conhecimento adicional de bancos de dados locais, garantindo a privacidade e a segurança dos dados.
- **Custo-eficiência**: Sob a restrição de privacidade dos dados, o RAG pode fornecer conhecimento essencial ao agente sem a necessidade de treinar um novo modelo fundamental totalmente, reduzindo assim os custos de treinamento.

### Desvantagens
- **Sobrecarga de manutenção**: A manutenção e atualização do conhecimento parametrizado no banco de dados vetorial requerem custos adicionais de computação e armazenamento.
- **Limitação de dados**: Os agentes ainda dependem principalmente dos dados com os quais foram treinados para gerar prompts, o que pode impactar a qualidade e a precisão do conteúdo gerado em domínios específicos.

## Usos Conhecidos
- **LinkedIn**: O LinkedIn aplica RAG para construir a pipeline de agentes baseados em modelos fundamentais, que podem buscar estudos de caso apropriados para responder aos usuários. 
- **Yan et al.** desenvolveram um avaliador de recuperação que pode gerar um grau de confiança após avaliar a qualidade dos dados recuperados, melhorando a robustez e o desempenho geral do RAG para agentes.
- **Levonian et al.** aplicaram RAG com GPT-3.5, desenvolvendo um agente que pode recuperar conteúdos de um livro didático de matemática de alta qualidade de código aberto para gerar respostas a alunos.



#TUTORIAL


# Agentic Workflow RAG-With-LangGraph-AstraDB-And-Llama-3.1
In this Blog we will build a multi AI agent with RAG using Langraph and AstraDB with integration with the Llama 3.1 open source model using Groq API. 
# Building Applications with Langchain and AstraDB

This project demonstrates how to build applications leveraging Langchain, a powerful framework for Large Language Model (LLM) applications, and AstraDB, a managed cloud database service. We will also introduce LangGraph, a library for managing workflows visually in LLM projects.

## Table of Contents

- [Introduction](#introduction)
- [Understanding Langchain](#understanding-langchain)
- [Introducing LangGraph](#introducing-langgraph)
- [Introducing AstraDB](#introducing-astraDB)
- [Project Setup](#project-setup)
  - [Connecting to AstraDB](#connecting-to-astraDB)
  - [Libraries Used](#libraries-used)
  - [Loading and Processing Web Documents](#loading-and-processing-web-documents)
  - [Creating Embeddings](#creating-embeddings)
  - [Setting Up a Vector Store](#setting-up-a-vector-store)
  - [Adding Documents to the Vector Store](#adding-documents-to-the-vector-store)
  - [Querying the Vector Store](#querying-the-vector-store)
  - [Routing User Queries](#routing-user-queries)
- [Conclusion](#conclusion)

## Introduction

In the rapidly evolving world of natural language processing (NLP), leveraging the power of Large Language Models (LLMs) is essential for developing intelligent applications. This README outlines the steps to build such applications using Langchain and AstraDB.

## Understanding Langchain

### What is Langchain?

Langchain is an open-source framework designed to assist developers in creating applications that utilize LLMs. It offers tools for managing prompts, integrating data sources, and chaining different NLP tasks.

### Key Features of Langchain

- **Prompt Management**: Tools for optimizing interactions with LLMs.
- **LLM Chains**: Workflows where the output of one LLM becomes the input for another task.
- **Memory**: Incorporate memory for context retention across interactions.
- **Integration**: Connect with APIs, databases, and data sources.
- **Agent Framework**: Develop intelligent agents that autonomously decide actions based on user input.

## Introducing LangGraph

### What is LangGraph?

LangGraph is a newer library that offers a graph-based approach to managing language models, allowing users to create and manage workflows visually.

### Key Features of LangGraph

- **Graph-Based Workflow**: Visualize data flow and tasks in LLM applications.
- **Easy Integration**: Helps integrate LLMs with various tools and databases.
- **Scalability**: Manages and scales LLM applications effectively.

## Introducing AstraDB

AstraDB is a managed cloud database service built on Apache Cassandra, offering scalability and reliability without manual infrastructure management.

### What is a Vector Database?

A vector database stores high-dimensional vector data, crucial for efficiently handling embeddings generated by machine learning models. Benefits include rapid similarity search and seamless integration with AI-powered applications.

## Project Setup

### Connecting to AstraDB

To begin, connect to AstraDB with the following code:

```python
import cassio

# Connection to AstraDB
ASTRA_DB_APPLICATION_TOKEN = "token"  # Enter the AstraCS string from your Token JSON file
ASTRA_DB_ID = "databaseID"  # Copy the Database ID from your AstraDB instance
cassio.init(token=ASTRA_DB_APPLICATION_TOKEN, database_id=ASTRA_DB_ID)

