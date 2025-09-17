# 17th-Sept-2025-AI-Summit
memo of something learned!

5:30 – 6:00 PM → Meet & Greet + Light Snacks
6:00 – 6:30 PM → AI Security with Siyavash
6:30 – 7:15 PM → Multi-Agent Systems with Eze
7:15 – 7:30 PM → Networking Wrap-Up

FEATURED SPEAKERS:
Siyavash Nia

AI Security: Balancing Innovation and Risk

    Session looks at the security considerations that come with the growing use of AI. We’ll discuss common risks such as data integrity, adversarial inputs, and system vulnerabilities—along with the opportunities AI brings to improve threat detection and response.

    - How to secure your LLM based AI system?
        - Accoustic and LLM AI?
        100 words vs 32K tokens.
        LLM (non-deterministic) vs traditional control(deterministic)

        RAG (external data source)
        MCP (Gateway)
        Agent (Action)

        Fine-tuning "could" leak data <-- Security issue
            privacy-prserving
            pre-process (annonymized)
            access control

        Attack vecotor
            ask
                summarize
                hidden
                penetrating words
            RAG
                Is the data clean?
                Phantom

            Connector
                Make system instruction hard to override

            Prompt
                embedding
                encoding
                *sanitization (check output from LLM)

            Monitor
                log
                rate limiting

            Vendor
                98.86% are volunerable........................

            AuthN & AuthZ
                LLM cannot be controlled under traditional way.

    
        1.Where is the LLM you used hosted at for finding the bank account and breached?

Ezequiel (Eze) Lanza

    Eze is working on cutting-edge multi-agentic systems with VLM (Vision-Language Models).
    He will showcase a multi-agent demo and dive into frameworks like beeai, ACP, and A2A, 
    while also exploring multimodal optimization with Hugging Face (HF).
    His talk will highlight practical approaches to combining text and vision models for powerful new AI workflows.

    https://github.com/zhuo-yoyowz/cvpr-2025

    - Multimodal RAG: Vision-language grounding with retrieval and agentic workflows.
    - Data prep: Local instruction dataset preparation, privacy-aware workflows.
    - Fine-tuning: Embedding models (BridgeTower) and LVLMs (Llama‑3.2‑11B‑Vision‑Instruct).
    - Retrieval: Vector databases; LlamaIndex/LangChain for efficient retrieval.
    - Deployment: OpenVINO optimization for low-latency inference on AI PCs/edge.
    - Use cases: Video Q&A, personalized shopping, education scenarios.

    VLM (Vision like pictures and movies)

        Mutilmodal RAG pipeline

            Models in this Collection:

                Llama-3.2-11B-Vision
                Llama-3.2-11B-Vision-Instruct
                Llama-3.2-90B-Vision
                Llama-3.2-90B-Vision-Instruct

        Challenge: running localhost

            GPU utilization is a key.

        Optimum-intel https://github.com/huggingface/optimum-intel
            
            open-source toolkit that enables high performance inference capabilities for Intel CPUs, GPUs, and special DL inference accelerators 

            OpenVINO INT8 (POT/NNCF)

            Quantization
                - Goal: Shrink and speed up models by lowering precision and removing redundancy while keeping accuracy acceptable.
                    - Q: keeping accuracy acceptable?
                    - Q: Does quantization apply for physics or math academic field????
                    - for weight and activation
