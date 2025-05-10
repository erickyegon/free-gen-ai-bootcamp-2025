# GenAI Language Learning Platform - Functional Requirements

## Business Goal
The Japanese Language Learning School seeks to extend their language offerings and augment the learning experience for students between instructor-led classes using GenAI solutions. The platform will integrate with their existing learning portal and learning record store, providing AI-powered learning applications while maintaining data privacy through on-premises infrastructure.

## System Overview
The GenAI Language Learning Platform is designed to facilitate language acquisition through AI-powered study activities and interactive learning experiences. The system leverages a core vocabulary database, retrieval-augmented generation (RAG), and large language models to provide personalized language learning activities.

## Data Strategy
- System must purchase and supply copyrighted language learning materials
- All materials must be properly licensed and stored in a secure database
- Content usage must comply with educational fair use guidelines
- Purchased materials must be properly attributed when used in learning activities

## Infrastructure Requirements
- System must operate on self-hosted infrastructure with an investment budget of 10-15K
- Infrastructure must support 300 active students located within Nagasaki city
- Solution must use open-source LLMs that can run effectively on the specified hardware budget
- Single server setup connected to the internet from the office location

## Core Functional Requirements

### 1. Language Portal & Word Group Management
- System must maintain a database of core 2000 vocabulary words
- Users must be able to access the Language Portal to view available word groups
- System must organize vocabulary into logical word groups for structured learning
- Teachers must be able to manage and customize word groups for their students
- System must integrate with the school's existing learning portal

### 2. Study Activities Engine
- System must support multiple study activity types:
  - Sentence Constructor exercises
  - Writing practice applications
  - Light Visual Novel Reading experiences
  - Text Adventure Immersion Games
  - Visual Flashcard Vocabulary practice
  - Speech-to-Listen exercises
- Each activity must be designed to enhance specific language learning skills
- Activities must provide personalized difficulty based on student progress

### 3. RAG (Retrieval Augmented Generation) Capabilities
- System must implement RAG to enhance language generation quality
- RAG component must be able to query the Vector Database to retrieve relevant language examples
- RAG must connect to external internet resources when additional context is needed
- System must maintain a Prompt Cache to optimize performance of common queries
- RAG implementation must be optimized to run efficiently on the specified hardware

### 4. LLM Integration
- System must use IBM Granite as the primary LLM ([IBM Granite on Hugging Face](https://huggingface.co/IBM/granite-7b-base))
- IBM Granite must be selected for its open-source nature and traceable training data
- Model selection ensures transparency and helps avoid copyright issues
- Input Guardrail must validate and sanitize all user inputs before processing
- Output Guardrail must ensure all LLM responses are appropriate, accurate, and educational
- LLM must be capable of multilingual support to facilitate expansion to other languages

### 5. User Interaction Flow
- System must accept natural language queries from users
- Queries must be processed through the RAG system to enhance context
- System must deliver coherent, educational responses to user queries
- All user-system interactions must be tracked for personalized learning
- System must integrate with the school's existing learning record store

### 6. Database Requirements
- Core 2000 words database must be maintained and regularly updated
- Vector Database must store embeddings for efficient semantic search
- System must implement efficient database querying for real-time interactions
- Student progress data must be securely stored and synchronized with the main learning record store
- Properly licensed teaching materials must be stored and indexed for retrieval

### 7. Internet Connectivity
- System must be able to access internet resources when needed
- Connection to external resources must be secure and privacy-compliant
- System must gracefully handle offline scenarios with cached resources
- Internet bandwidth usage must be optimized to function effectively with the office connection

### 8. Multi-user Support
- System must support both student and teacher user roles
- Teachers must have additional capabilities for content management
- Student progress must be tracked individually across all study activities
- System must accommodate simultaneous usage by multiple students

### 9. System Performance
- Study activity response time must not exceed 2 seconds
- System must handle concurrent users without performance degradation
- RAG query processing must be optimized for educational real-time interactions
- System must effectively utilize available hardware resources

### 10. Multi-language Support
- Initial implementation must focus on Japanese language learning
- Architecture must be designed to enable extension to additional languages
- Language-specific resources must be modular and easily configurable
- System must handle different character sets and writing systems

## Implementation Priorities
1. Core database and word group management
2. RAG implementation with vector database integration
3. Basic study activities (Sentence Constructor, Flashcards)
4. IBM Granite integration with guardrails
5. Advanced study activities (Visual Novel, Text Adventure)
6. Teacher management features
7. Performance optimization and scaling
8. Multi-language support framework

## Technical Dependencies
- IBM Granite open-source language model (7B parameter version) - https://huggingface.co/ibm-granite
- Vector database technology optimized for self-hosting
- Secure internet access with appropriate bandwidth
- User authentication system that integrates with existing portal
- Educational content management system
- Licensed language learning materials database
