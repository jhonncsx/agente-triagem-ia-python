# 🤖 Agente de Triagem e Roteamento Automático com IA

Pipeline de automação desenvolvido em **Python** que utiliza **Inteligência Artificial Generativa (Google Gemini)** e validação de esquemas (**Pydantic**) para transformar mensagens desestruturadas de clientes em dados JSON padronizados, classificando urgência e disparando ações de roteamento automático.

---

## 🎯 Problema Resolvido
Equipes de operações e suporte perdem horas lendo mensagens longas e desorganizadas (e-mails, formulários, WhatsApp) para decidir para qual setor encaminhar cada demanda e qual prioridade dar. Este agente automatiza 100% da leitura, extração de entidades e roteamento inicial.

## ⚙️ Arquitetura do Fluxo
1. **Entrada:** Recebe texto bruto e não estruturado.
2. **Processamento Cognitivo (LLM):** Envia o conteúdo para a API do `gemini-2.5-flash` com baixa temperatura (`0.1`) para máxima consistência.
3. **Structured Outputs (Pydantic):** Garante que a resposta da IA siga rigorosamente um contrato de dados (`JSON Schema`), eliminando quebras de integração.
4. **Ação Automática:** Roteia o ticket para a fila correta e dispara alerta prioritário em casos de urgência **Alta**.

## 🛠️ Tecnologias Utilizadas
* **Python 3.10+**
* **Google GenAI SDK (`google-genai`)** — Integração com modelos Gemini.
* **Pydantic** — Validação de dados e tipagem estrita para saídas estruturadas.
* **Python-Dotenv** — Gerenciamento seguro de variáveis de ambiente.

## 🚀 Como Executar Localmente

1. Clone o repositório:
   ```bash
   git clone [https://github.com/jhonncsx/agente-triagem-ia-python.git](https://github.com/jhonncsx/agente-triagem-ia-python.git)
   cd agente-triagem-ia-python
