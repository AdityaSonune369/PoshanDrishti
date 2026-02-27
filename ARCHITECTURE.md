# Architecture Diagram

```mermaid
flowchart LR
    subgraph "User Interface"
        UI[Gradio UI<br/>Animated + Responsive]
    end
    
    subgraph "Perception"
        Vision[BLIP + OpenCV<br/>Food & Health Check]
    end
    
    subgraph "Intelligence"
        LLM[Phi-3-mini-4k<br/>Personalised Plan]
    end
    
    subgraph "Delivery"
        Out[Voice + Score<br/>+ PDF Export]
    end
    
    subgraph "AMD Foundation"
        AMD[AMD Ryzen AI<br/>Software Stack 1.7]
    end

    UI --> Vision
    Vision --> LLM
    LLM --> Out
    AMD -.-> Vision & LLM

    style UI fill:#0f766e,stroke:#facc15,stroke-width:3px,color:#fff
    style AMD fill:#1e40af,stroke:#facc15,stroke-width:3px,color:#fff
