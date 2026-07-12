# Vera — Assistente de Relacionamento Financeiro Inteligente

> Projeto do Lab **"Construa Seu Assistente Virtual Com Inteligência Artificial"** (DIO).

## 1. O que é a Vera

Vera é um assistente virtual conversacional voltado ao **relacionamento financeiro** de clientes de um banco digital. Ela conversa em linguagem natural, entende a necessidade da pessoa usuária e responde com base em uma base de conhecimento organizada — sem inventar informações.

## 2. Para quem serve

- **Público-alvo:** clientes de um banco digital que têm dúvidas simples sobre produtos financeiros (poupança, CDB, cartão de crédito, empréstimo) ou querem simular cálculos financeiros básicos (juros, financiamento).
- **Time interno:** também serve como referência para a equipe de experiência do cliente entender como uma IA generativa pode reduzir a carga de perguntas repetitivas no atendimento humano.

## 3. Como a Vera deve se comportar

| Princípio | Como é aplicado |
|---|---|
| Clareza | Respostas curtas, linguagem simples, sem jargão bancário desnecessário |
| Honestidade | Nunca inventa números, taxas ou condições — usa apenas a base de conhecimento |
| Transparência sobre limites | Se não houver informação suficiente, a Vera diz isso e sugere um próximo passo (ex: falar com atendimento humano) |
| Segurança | Não pede nem armazena dados sensíveis (CPF, senha, número de cartão) |
| Foco em decisão | Toda resposta termina indicando uma ação ou próximo passo possível para a pessoa usuária |

## 4. Funcionalidades

- **FAQs inteligentes** — respostas para dúvidas frequentes sobre produtos e serviços.
- **Cálculos financeiros demonstrativos** — simulação de juros simples, juros compostos e financiamento parcelado (valores ilustrativos, não são recomendações de investimento).
- **Explicações de produtos** — descrição simples de produtos financeiros disponíveis na base.
- **Persistência de contexto** — a conversa lembra o que foi perguntado antes na mesma sessão (ex: "e para 12 meses?" depois de uma simulação).

## 5. Estrutura do repositório

```
assistente-virtual-ia/
  README.md              → este arquivo (documentação geral)
  data/
    base_conhecimento.md → base de conhecimento (FAQs, produtos, fórmulas)
  docs/
    prompts.md            → prompts que orientam o comportamento da IA
    avaliacao.md           → como as respostas foram avaliadas
    pitch.md                → pitch do projeto
  src/
    index.html            → protótipo funcional (chat) executável no navegador
```

## 6. Como executar o protótipo

1. Abra `src/index.html` diretamente no navegador (não precisa de servidor).
2. Digite uma pergunta no campo de texto (ex: "o que é CDB?" ou "simular financiamento de 5000 em 10x").
3. A Vera responde com base no arquivo `data/base_conhecimento.md`, incorporado no próprio `index.html`.

> Este protótipo usa correspondência de palavras-chave sobre a base de conhecimento para simular o comportamento de um assistente de IA generativa, priorizando a demonstração do fluxo (entender → consultar base → responder → indicar próximo passo). Em uma versão de produção, o núcleo de linguagem natural seria substituído por uma chamada real a um modelo de IA generativa (ex: API da Anthropic), mantendo a mesma base de conhecimento e as mesmas restrições descritas em `docs/prompts.md`.

## 7. Limitações conhecidas

- Não é um simulador financeiro oficial; os cálculos são apenas demonstrativos.
- A base de conhecimento é pequena e cobre poucos produtos, propositalmente, para manter o escopo do protótipo simples.
- Não há integração com sistemas reais do banco, autenticação ou dados de clientes reais.
