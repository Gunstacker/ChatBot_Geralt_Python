# 🧙‍♂️ Chatbot Inteligente – Geralt de Rívia (Llama 3.1 • Groq API)

Este projeto implementa um **chatbot inteligente** capaz de interpretar o personagem **Geralt de Rívia**, mantendo seu estilo de fala, sarcasmo, comportamento pragmático e coerência durante toda a interação.  

O chatbot utiliza um modelo **Llama 3.1** rodando via **Groq API**, integrado a uma interface gráfica desenvolvida com **Gradio**.

Todo o projeto foi desenvolvido para funcionar **exclusivamente no Google Colab**, sem necessidade de instalar dependências locais ou configurar API Key — **o arquivo já inclui tudo o que é necessário para execução**.

---

## 🚀 Tecnologias Utilizadas

- Python 3.10+
- Groq API (Llama 3.1)
- Gradio – Interface Web
- Google Colab – Ambiente de Execução
- Dataclasses – Organização da Lógica do Personagem

---

# ⚠️ Como Executar o Projeto (IMPORTANTE)

Este chatbot foi construído para ser executado **única e exclusivamente no Google Colab**.

Você **não precisa**:
- instalar nada no seu computador  
- configurar API Key  
- alterar caminhos ou dependências  

Basta rodar o arquivo `.py` no Colab.

---

# ▶️ Passo a Passo – Execução no Google Colab

## **1. Acesse o Google Colab**
https://colab.research.google.com

---

## **2. Faça upload do arquivo `chatbot_groq.py`**
No painel lateral esquerdo:

Files → Upload → selecione chatbot_groq.py

yaml
Copiar código

---

## **3. Instale as dependências necessárias**

Em uma célula nova, execute:

```python
!pip install gradio groq --quiet
4. Execute o chatbot
Rode:

python
Copiar código
!python chatbot_groq.py
Se tudo estiver correto, aparecerá:

perl
Copiar código
Chatbot iniciado com sucesso! Acesse o link abaixo:
http://127.0.0.1:7860/
Clique no link para abrir a interface Gradio.

💬 Como Usar o Chatbot
A interface é simples e intuitiva:

Digite sua mensagem na caixa de texto

Selecione o humor do personagem (Neutro, Calmo, Irritado, Sarcástico)

Veja as respostas aparecerem na janela de chat

Clique em “Limpar conversa” para reiniciar

O chatbot responde exatamente como Geralt, mantendo:

frases curtas

humor seco

impaciência característica

comportamento coerente

🧰 Personalização (Opcional)
Você pode alterar o personagem editando o bloco:

python
Copiar código
character = CharacterConfig(
    name="Geralt de Rívia",
    description="...",
    speaking_style="...",
    behavior_rules="..."
)
Ou trocar o modelo usado pela API:

python
Copiar código
MODEL = "llama-3.1-8b-instant"
Mas nada disso é necessário para rodar o projeto — já está tudo configurado.

📁 Estrutura do Repositório
bash
Copiar código
/chatbot-llama
│
├── chatbot_groq.py      # Arquivo principal do chatbot (executar no Colab)
└── README.md            # Este documento
👥 Integrantes do Grupo
Augusto — Arquitetura do chatbot, integração com LLM, engenharia de prompt
Matheus — Interface Gradio, fluxo de mensagens e histórico
Átila — Testes, validação da personalidade e documentação

✔ Status do Projeto
100% funcional, aprovado e pronto para apresentação.

📌 Observações Finais
Não é necessário criar ou inserir API Keys.

O projeto já está configurado internamente.

Execute exatamente no Google Colab para evitar problemas.

O processamento do modelo ocorre na nuvem via Groq, garantindo velocidade.