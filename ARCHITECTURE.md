# Architecture Diagram

```mermaid
flowchart LR
    A[Gradio UI] --> B[BLIP + OpenCV]
    B --> C[Phi-3-mini-4k]
    C --> D[Voice + PDF + Score]
    E[AMD Ryzen AI Stack 1.7] -.-> B & C
