# 💼 Guardião de Caixa

Agente financeiro inteligente com IA generativa, focado em **gestão de caixa para pequenos negócios**, como **MEIs, autônomos e microempresas**.

O projeto foi desenvolvido como um protótipo funcional capaz de analisar dados mockados de clientes PJ, interpretar o contexto financeiro do negócio e responder de forma consultiva, preventiva e segura.

---

## Contexto

No setor financeiro, os assistentes virtuais estão evoluindo de simples chatbots reativos para **agentes inteligentes e contextuais**, capazes de:

- antecipar riscos financeiros;
- personalizar recomendações com base no perfil e no momento do cliente;
- orientar decisões práticas no dia a dia do negócio;
- responder com mais segurança, evitando alucinações.

O **Guardião de Caixa** foi criado com esse objetivo: atuar como um **CFO digital** para pequenos empreendedores, ajudando na leitura do fluxo de caixa, no acompanhamento de vencimentos, no controle de retiradas e na organização financeira da operação.

---

## Objetivo do Agente

O Guardião de Caixa ajuda o cliente a:

- entender a situação atual do caixa;
- acompanhar entradas e saídas;
- visualizar contas a pagar e a receber;
- identificar riscos de aperto financeiro;
- receber alertas preventivos;
- tomar ações práticas para preservar a saúde do negócio.

O agente responde com base exclusiva na base mockada do projeto e mantém o foco em **clareza, coerência e segurança**.

---

## Principais Funcionalidades

- Chat interativo com interface em **Streamlit**
- Integração com modelo local via **Ollama**
- Uso de dados mockados em **CSV** e **JSON**
- Montagem dinâmica de contexto por cliente
- Histórico de conversa separado por cliente
- Continuidade contextual com uso do histórico no prompt
- Recomendações práticas baseadas em fluxo de caixa
- Respostas com restrição de escopo e comportamento anti-alucinação

---

## Tecnologias Utilizadas

| Categoria | Ferramenta |
|-----------|------------|
| Interface | Streamlit |
| LLM local | Ollama |
| Linguagem | Python |
| Manipulação de dados | Pandas |
| Base de conhecimento | JSON + CSV |
| Integração HTTP | Requests |

---

## Estrutura do Repositório

```text
DIO-LAB-BIA-DO-FUTURO/
│
├── README.md
│
├── assets/
│
├── data/
│   ├── clientes_pj.json
│   ├── contas_pagar.csv
│   ├── contas_pj.json
│   ├── contas_receber.csv
│   ├── historico_atendimento.csv
│   ├── historico_interacoes.csv
│   ├── indicadores_caixa.json
│   ├── metas_financeiras.json
│   ├── perfil_investidor.json
│   ├── produtos_bancarios_pj.json
│   ├── produtos_financeiros.json
│   ├── regras_alertas.json
│   ├── transacoes_pj.csv
│   └── transacoes.csv
│
├── docs/
│
├── examples/
│
└── src/
    ├── app.py
    └── README.md
