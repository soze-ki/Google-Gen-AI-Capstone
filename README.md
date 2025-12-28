## Capstone Project for 5-day Gen AI Intensive Course with Google (Apr 2025)

This notebook demonstrated the creation of a Web3 Security Researcher AI Assistant using Google's Gemini Pro model. Key capabilities included:

Direct LLM Interaction: Successfully used the google-generativeai library to analyze Solidity code based on a detailed system prompt and contextual information.
Function Calling Simulation: Implemented custom Python tools (VulnerabilityAnalysisTool, GasOptimizerTool) using langchain-core's BaseTool structure, simulating function calling by running these tools directly and feeding their structured output (JSON) into the LLM prompt.
RAG Implementation: Created a knowledge base of vulnerabilities, generated embeddings using models/embedding-001, performed similarity searches, and included retrieved context in the LLM prompt to enhance analysis accuracy.
Challenges & Workarounds: Significant challenges were encountered with the langchain-google-genai library wrapper within the Kaggle environment, leading to persistent hangs during API calls. Workarounds like setting NO_GCE_CHECK=True resolved issues for direct library calls but not for the LangChain wrapper. Consequently, the primary analysis pathway uses direct SDK calls.

Future Work:

Resolve LangChain wrapper compatibility issues (possibly requiring library updates or reporting bugs).
Expand the vulnerability knowledge base and RAG capabilities.
Integrate more sophisticated static analysis techniques (e.g., Slither output) as tool inputs.
Develop more comprehensive evaluation metrics.
Explore integration with on-chain data via blockchain explorers.
