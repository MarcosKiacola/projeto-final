# Avaliação e Métricas — Vera

## Como a Vera foi testada

Foram testados casos manuais cobrindo os principais comportamentos esperados: FAQ, simulação de cálculo, pedido de dado faltante, contexto de conversa e ausência de informação.

| # | Entrada de teste | Comportamento esperado | Resultado |
|---|---|---|---|
| 1 | "o que é CDB?" | Responder com definição da base, sem inventar taxas | ✅ Passou |
| 2 | "simular juros compostos de 1000 em 6 meses" | Calcular e mostrar disclaimer de valor fictício | ✅ Passou |
| 3 | "simular financiamento de 5000 em 10x" | Calcular parcela simples sem juros | ✅ Passou |
| 4 | "quero simular" (sem valor/prazo) | Pedir os dados faltantes em vez de inventar | ✅ Passou |
| 5 | "e para 12 meses?" (após simulação anterior) | Reaproveitar tipo/valor do contexto anterior | ✅ Passou |
| 6 | "perdi meu cartão" | Orientar bloqueio pelo app | ✅ Passou |
| 7 | "qual a cotação do dólar hoje?" | Reconhecer que não tem essa informação e indicar atendimento humano | ✅ Passou |

## Critérios de qualidade avaliados

- **Ausência de alucinação:** a resposta usa apenas dados presentes em `data/base_conhecimento.md`?
- **Clareza:** a resposta é curta e compreensível sem jargão?
- **Indicação de limite:** quando falta informação, a Vera avisa isso explicitamente em vez de arriscar uma resposta?
- **Próximo passo:** toda resposta indica uma ação seguinte para a pessoa usuária?
- **Persistência de contexto:** perguntas de acompanhamento reaproveitam informações da mensagem anterior?

## Limitações da avaliação

- Os testes foram feitos manualmente, digitando os casos no protótipo — não há testes automatizados neste momento.
- A detecção de intenção é baseada em palavras-chave, então frases fora do padrão testado podem não ser reconhecidas corretamente. Isso é uma limitação conhecida do protótipo (ver README, seção "Limitações").
- Numa versão com IA generativa real (API), a cobertura de linguagem natural seria maior, mas os mesmos critérios de avaliação (sem alucinação, honestidade sobre limites, foco em próximo passo) continuariam sendo os principais indicadores de qualidade.
