# AI assistant for Zubin
This is a AI assistant bot developed based on `Retrieval-Augmented Generation`(RAG). 

## What is RAG?
LLMs are trained on a large but fixed corpus of data, limiting their ability to reason about private or recent information. Retrieval augmented generation (RAG) has emerged as a popular and powerful mechanism to expand an LLM's knowledge base, using documents retrieved from an external data source to ground the LLM generation via in-context learning. 
![rag_detail_v2](https://github.com/langchain-ai/rag-from-scratch/assets/122662504/54a2d76c-b07e-49e7-b4ce-fc45667360a1)

## Technical Stack
- LLM server: Ollama
- Model:  mistral:latest
- Language Model Integration Framework: LangChain
- Web framework for API: FASTAPI

## How it works?
![屏幕截图 2024-08-25 200023](https://github.com/user-attachments/assets/c50d24a7-89d1-4845-b51a-1c2896390177)

## Env requirement
- `pip install -r requirements.txt`
- get your langchain API Key on openai, you may need to [register] (VPN required) here, and set it in `.env.example`, copying required .env file
   - `cp -RPp .env.example .env`(MacOs or Linux)
   - `copy .env.example .env`(windows)

### Ollama Model
Refer to [Ollama] for more information. Make sure it is running as a service.
- `pip install ollama` (ollama --version: 0.3.6)
- `ollama run mistral:latest`
- Check your model with `ollama list`

## Knowledge
You can change the `./data/lnowledge.md` knowledge base for your bot. Here I am using book of `The Wealth of Nations`. [Source]
## Start the server
- `uvicorn main:app --reload`

## Try it!
<img width="353" alt="image" src="https://github.com/user-attachments/assets/5b576179-d09d-46d2-ac56-6f3544b8d0df">

### Other reference:
- [LangChain API Key Guide]

[Langchain]:https://python.langchain.com/v0.2/docs/integrations/text_embedding/ollama/
[Ollama]:https://ollama.com/
[LangChain API Key Guide]:https://www.restack.io/docs/langchain-knowledge-langchain-api-key-guide
[register]: https://platform.openai.com/
[Technical method]:https://juejin.cn/post/7378779608353669158
[Source]: https://github.com/mlschmitt/classic-books-markdown/tree/main
