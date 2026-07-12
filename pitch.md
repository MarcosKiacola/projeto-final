# Pitch — Vera, Assistente de Relacionamento Financeiro

## O problema

Bancos digitais recebem um alto volume de perguntas repetitivas — o que é um CDB, como bloquear um cartão, quanto rende uma simulação de juros. Grande parte disso não precisa de um atendente humano, mas hoje consome tempo de atendimento e gera fricção para quem só queria uma resposta rápida.

## A solução

A Vera é um assistente conversacional que entende a dúvida da pessoa usuária, consulta uma base de conhecimento organizada e responde de forma simples e honesta — sem inventar taxas ou condições, e avisando quando não sabe algo. Ela também faz simulações financeiras demonstrativas (juros e financiamento) e mantém o contexto da conversa, permitindo perguntas de acompanhamento naturais.

## O valor

- **Para o cliente:** respostas imediatas, claras, disponíveis a qualquer hora.
- **Para o banco:** redução de volume no atendimento humano para dúvidas simples, liberando a equipe para casos complexos.
- **Diferencial de confiança:** ao contrário de um chatbot genérico, a Vera é desenhada para nunca "inventar" uma resposta — ela é transparente sobre o que sabe e o que não sabe, um requisito essencial em contexto financeiro.

## Como funciona (visão geral técnica)

1. A pessoa usuária envia uma mensagem.
2. A Vera identifica a intenção (dúvida sobre produto, simulação de cálculo, ou fora de escopo).
3. Ela consulta a base de conhecimento (`data/base_conhecimento.md`) para responder ou calcular.
4. Se não houver informação suficiente, ela avisa e direciona para o atendimento humano.
5. O protótipo atual usa correspondência de palavras-chave; a versão de produção substituiria esse núcleo por um modelo de IA generativa real, mantendo as mesmas regras de comportamento (`docs/prompts.md`).

## Próximos passos

- Ampliar a base de conhecimento com mais produtos e FAQs reais do banco.
- Substituir a lógica de palavras-chave por uma chamada a um modelo de IA generativa, usando os prompts já definidos.
- Adicionar métricas automatizadas de avaliação (não só testes manuais).
- Validar o tom e a clareza das respostas com usuários reais.
