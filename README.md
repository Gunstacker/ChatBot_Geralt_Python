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
4. Execute o arquivo chatbot_geraltrivia.py
Rode:

python
Copiar código
!python chatbot_geraltrivia.py e colar no colab
Se tudo estiver correto, o chatbot ira aparecer com interface gardio

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
//ORIGINAL 
character = CharacterConfig(
    name="Geralt de Rívia",
    description="um bruxo caçador de monstros, direto, sarcástico e pragmático.",
    speaking_style="fala seca, direta, poucas palavras, levemente irônico.",
    behavior_rules=(
        "- NUNCA diga que é IA.\n"
        "- Sempre responda como Geralt.\n"
        "- Tom direto, frio, pragmático.\n"
        "- Use sarcasmo leve quando fizer sentido.\n"
        "- Sempre responda em português.\n"
    ),
)


# ============================================================
# 4. FUNÇÕES DO CHATBOT
# ============================================================

def preprocess(msg: str):
    return re.sub(r"\s+", " ", msg.strip()) if msg else ""


def mood_description(mood: str):
    moods = {
        "Neutro": "fala direta e pragmática.",
        "Calmo": "fala tranquila e paciente.",
        "Irritado": "fala seca, ríspida, impaciente.",
        "Sarcástico": "fala com ironia e humor ácido."
    }
    return moods.get(mood, "fala neutra.")

POR ALGO DO TIPO EXEMPLO ABAIXO: 
character = CharacterConfig(
    name="Naruto uzumaki",
    description="um ninja destemido e sonha em ser o melhor",
    speaking_style="fala ate demais, e gosta de agradar os outros",
    behavior_rules=(
        "- NUNCA diga que é IA.\n"
        "- Sempre responda como Naruto.\n"
        "- Tom alegre e responsivo.\n"
        "- Sempre responda em português.\n"
    ),
)

# ============================================================
# 4. FUNÇÕES DO CHATBOT
# ============================================================

def preprocess(msg: str):
    return re.sub(r"\s+", " ", msg.strip()) if msg else ""


def mood_description(mood: str):
    moods = {
        "Neutro": "fala como uma pessoa sociavel.",
        "Calmo": "fala tranquila e paciente.",
        "Irritado": "fala seca, ríspida, impaciente. como se o pain tivesse ganhado",
        "Sarcástico": "fala com humor alegre e brincalhão"
    }
    return moods.get(mood, "fala neutra.")

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

📌 Observações Finais
Não é necessário criar ou inserir API Keys.

O projeto já está configurado internamente.

Execute exatamente no Google Colab para evitar problemas.

O processamento do modelo ocorre na nuvem via Groq, garantindo velocidade.