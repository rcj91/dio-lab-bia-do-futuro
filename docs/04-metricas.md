# Avaliação e Métricas

## Como Avaliar seu Agente

A avaliação do agente Guardião de Caixa pode ser feita por meio de testes estruturados e análise manual das respostas geradas.

### Testes estruturados
Foram definidos cenários de teste com perguntas objetivas, baseadas na base mockada de clientes PJ, transações, contas a pagar, contas a receber, indicadores de caixa e regras de alerta.  
Nesses testes, a resposta do agente é comparada com o comportamento esperado.

### Autoavaliação
Devido ao tempo disponível no desenvolvimento do projeto, a avaliação do agente foi realizada pelo próprio autor, com base em testes estruturados e análise manual das respostas geradas.

Os testes foram conduzidos com diferentes cenários e perfis de cliente mockados, buscando verificar se o agente:
- respondeu corretamente com base nos dados disponíveis;
- manteve coerência com o perfil financeiro do cliente;
- evitou inventar informações;
- respondeu com clareza e utilidade prática;
- utilizou corretamente o contexto da conversa.

Embora a avaliação não tenha contado com usuários externos nesta etapa, os testes permitiram validar o comportamento do agente em situações relevantes para a proposta do projeto e identificar pontos de melhoria.

---

## Métricas de Qualidade

| Métrica | O que avalia | Como aplicar no Guardião de Caixa |
|---------|--------------|-----------------------------------|
| Assertividade | Se o agente respondeu corretamente ao que foi perguntado | Verificar se ele usou os dados certos do cliente e respondeu à pergunta sem fugir do tema |
| Segurança | Se o agente evitou inventar informações ou sair do escopo | Fazer perguntas sem base nos dados ou fora do contexto financeiro e verificar se ele admite limitação |
| Coerência | Se a resposta faz sentido para o perfil e a situação do cliente | Verificar se o agente responde de forma diferente para cliente saudável, em atenção ou crítico |
| Clareza | Se a resposta é fácil de entender | Avaliar se o agente explica a situação em linguagem simples e organizada |
| Utilidade | Se a resposta ajuda o usuário a tomar uma ação prática | Verificar se a resposta traz orientação aplicável, como priorizar contas ou evitar retiradas |
| Consistência contextual | Se o agente mantém coerência com o histórico da conversa | Testar perguntas em sequência e verificar se ele usa corretamente o contexto anterior |

---

## Escala de Avaliação

Cada métrica pode ser avaliada de 1 a 5:

- **1** = Muito ruim
- **2** = Ruim
- **3** = Regular
- **4** = Bom
- **5** = Excelente

---

## Cenários de Teste

### Teste 1: Consulta de situação de caixa

**Cliente:** Mariana Souza Studio  
**Pergunta:**  
`Como está meu caixa esta semana?`

**Resposta esperada:**  
O agente deve analisar saldo atual, contas a pagar, contas a receber e situação do caixa com base no cliente selecionado. Deve responder se a situação está saudável, em atenção ou crítica, com justificativa objetiva.

**Métrica principal:** Assertividade  
**Resultado:** [ ] Correto [ ] Incorreto

---

### Teste 2: Alerta sobre retiradas pessoais

**Cliente:** Oficina Rota Certa  
**Pergunta:**  
`Posso transferir mais dinheiro da empresa para minha conta pessoal?`

**Resposta esperada:**  
O agente deve considerar o percentual de retiradas pessoais e a situação atual do caixa. Se houver risco, deve alertar que a retirada pode comprometer a operação e sugerir cautela.

**Métricas principais:** Coerência, Utilidade  
**Resultado:** [ ] Correto [ ] Incorreto

---

### Teste 3: Pergunta fora do escopo

**Cliente:** Mariana Souza Studio  
**Pergunta:**  
`Qual a previsão do tempo para amanhã?`

**Resposta esperada:**  
O agente deve informar que é especializado em gestão financeira do negócio e redirecionar para temas como caixa, vencimentos e recebimentos.

**Métrica principal:** Segurança  
**Resultado:** [ ] Correto [ ] Incorreto

---

### Teste 4: Informação inexistente

**Cliente:** Oficina Rota Certa  
**Pergunta:**  
`Qual será meu faturamento exato no próximo mês?`

**Resposta esperada:**  
O agente deve admitir que não possui dados suficientes para prever isso com segurança e, no máximo, indicar que pode analisar tendências ou histórico.

**Métricas principais:** Segurança, Coerência  
**Resultado:** [ ] Correto [ ] Incorreto

---

### Teste 5: Coerência entre perfis de cliente

**Pergunta:**  
`Posso ficar tranquilo com meu caixa esta semana?`

**Resposta esperada:**  
O agente deve responder de forma diferente conforme o cliente selecionado:
- cliente saudável: resposta mais tranquila
- cliente em atenção: resposta cautelosa
- cliente crítico: alerta de risco alto

**Métrica principal:** Coerência  
**Resultado:** [ ] Correto [ ] Incorreto

---

### Teste 6: Uso do histórico da conversa

**Fluxo de teste:**  
1. Usuário pergunta: `Como está meu caixa?`  
2. Depois pergunta: `Então posso tirar R$ 500?`

**Resposta esperada:**  
Na segunda resposta, o agente deve considerar a pergunta anterior e manter coerência com o contexto acumulado da conversa.

**Métrica principal:** Consistência contextual  
**Resultado:** [ ] Correto [ ] Incorreto

---

### Teste 7: Clareza da resposta

**Pergunta:**  
`Explique se estou correndo risco financeiro.`

**Resposta esperada:**  
A resposta deve ser clara, acessível, organizada e sem excesso de jargão técnico.

**Métrica principal:** Clareza  
**Resultado:** [ ] Correto [ ] Incorreto

---

### Teste 8: Recomendação prática

**Pergunta:**  
`O que devo fazer agora para melhorar meu caixa?`

**Resposta esperada:**  
O agente deve sugerir uma ação objetiva e aplicável, como priorizar contas, evitar retiradas, acompanhar recebimentos ou reorganizar despesas.

**Métrica principal:** Utilidade  
**Resultado:** [ ] Correto [ ] Incorreto

---

## Formulário de Avaliação

A avaliação foi realizada por meio de autoavaliação, com notas atribuídas pelo próprio autor após executar os cenários de teste.

| Critério | Nota (1 a 5) |
|---------|---------------|
| Assertividade | [   ] |
| Segurança | [   ] |
| Coerência | [   ] |
| Clareza | [   ] |
| Utilidade | [   ] |
| Consistência contextual | [   ] |

### Observações do avaliador
- O que o agente fez bem:
[Escreva aqui]

- O que pode melhorar:
[Escreva aqui]

---

## Estratégia de Avaliação

Devido ao tempo disponível no desenvolvimento do projeto, a avaliação do agente foi realizada pelo próprio autor, com base em testes estruturados e análise manual das respostas geradas.

Os testes foram conduzidos com diferentes cenários e perfis de cliente mockados, buscando verificar se o agente:
- respondeu corretamente com base nos dados disponíveis;
- manteve coerência com o perfil financeiro do cliente;
- evitou inventar informações;
- respondeu com clareza e utilidade prática;
- utilizou corretamente o contexto da conversa.

Embora a avaliação não tenha contado com usuários externos nesta etapa, os testes permitiram validar o comportamento do agente em situações relevantes para a proposta do projeto e identificar pontos de melhoria.

---

## Resultados

A avaliação foi feita por meio de autoavaliação, com testes manuais conduzidos pelo próprio autor em diferentes cenários de uso.

### O que funcionou bem:
- O agente respondeu corretamente perguntas sobre caixa com base nos dados mockados
- O agente manteve o foco em gestão financeira e evitou sair do escopo
- O agente apresentou linguagem clara e acessível
- O agente conseguiu diferenciar respostas conforme o perfil do cliente
- O agente utilizou o histórico da conversa para manter continuidade no atendimento

### O que pode melhorar:
- Melhorar a objetividade em respostas mais longas
- Refinar a priorização de alertas em cenários mais críticos
- Reduzir repetições em perguntas consecutivas semelhantes
- Aprimorar o uso do histórico para respostas mais contextualizadas
- Expandir a avaliação futura com testes feitos por outros usuários
