# Talking with my files

Este projeto implementa um chatbot baseado em **RAG (Retrieval-Augmented Generation)** usando **Streamlit** para interação, permitindo que usuários façam perguntas baseadas no conteúdo de documentos PDF.

## 📌 Funcionalidades
- Upload de arquivos **PDF** para extração de informações.
- Uso de **FAISS** para indexação vetorial e recuperação eficiente de documentos.
- Geração de **embeddings** com **Hugging Face Embeddings (BAAI/bge-m3)**.
- Suporte a diferentes modelos de linguagem, como **Hugging Face Hub** e **Ollama**.
- Histórico de chat armazenado para contexto de conversação.
- Respostas geradas pelo modelo com referência às fontes nos documentos.

## 🛠️ Tecnologias Utilizadas
- **Python**
- **Streamlit**
- **LangChain** (para configuração do RAG)
- **FAISS** (indexação e busca vetorial)
- **Hugging Face Embeddings** (transformação de texto em vetores)
- **PyPDFLoader** (extração de texto de PDFs)
- **Ollama / Hugging Face Hub** (modelos de linguagem para geração de respostas)

## 🚀 Como Executar
1. Clone este repositório:
   ```sh
   git clone https://github.com/seu-repositorio.git
   cd seu-repositorio
   ```
2. Instale as dependências:
   ```sh
   pip install -r requirements.txt
   ```
3. Configure suas credenciais (se necessário, por exemplo, para Hugging Face Hub ou OpenAI):
   ```sh
   export HUGGINGFACEHUB_API_TOKEN='seu_token_aqui'
   export OPENAI_API_KEY='seu_token_aqui'
   ```
4. Execute a aplicação:
   ```sh
   streamlit run app.py
   ```
5. Acesse no navegador: `http://localhost:8501`

## 📂 Estrutura do Projeto
```
📂 talking-with-my-files
├── app.py                 # Código principal
├── requirements.txt       # Dependências do projeto
├── .env                   # Variáveis de ambiente
├── 📂 vectorstore         # Armazena a base FAISS
└── README.md              # Documentação do projeto
```

## 📝 Como Funciona
1. O usuário faz upload de um ou mais arquivos **PDF**.
2. O conteúdo é processado e convertido em **vetores (embeddings)**.
3. A base de dados vetorial é criada e armazenada usando **FAISS**.
4. O usuário faz uma pergunta na interface.
5. O sistema busca os trechos mais relevantes no **FAISS**.
6. O modelo de linguagem selecionado gera uma resposta baseada nesses trechos.
7. A resposta é exibida junto com as fontes extraídas do documento.

## 📌 Possíveis Melhorias
- Suporte a mais tipos de arquivos (ex: `.txt`, `.docx`).
- Ajuste fino nos **modelos de embedding** para melhorar a recuperação de informações.
- Personalização da interface no Streamlit.

## 🤝 Contribuição
Sinta-se à vontade para abrir issues, enviar PRs ou sugerir melhorias!

---

🔗 **Contato**: [Seu Nome](https://linkedin.com/in/seu-perfil) | ✉️ Email: seuemail@example.com


