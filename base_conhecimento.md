# Base de Conhecimento — Vera

Esta base alimenta as respostas da Vera. Tudo o que a Vera responde deve vir daqui — nada é inventado.

## 1. FAQs

| Pergunta | Resposta |
|---|---|
| O que é CDB? | CDB (Certificado de Depósito Bancário) é um investimento de renda fixa em que você empresta dinheiro ao banco e recebe de volta com juros, em um prazo combinado. |
| O que é Pix? | Pix é o meio de pagamento instantâneo do Banco Central, disponível 24h por dia, usado para transferências e pagamentos entre contas. |
| Como aumento meu limite de cartão? | O limite de cartão é reavaliado periodicamente com base no seu relacionamento e uso. Não é possível solicitar aumento manual pelo assistente — fale com o atendimento humano para uma análise. |
| O que é a poupança? | A poupança é um investimento simples e de baixo risco, com rendimento mensal atrelado à taxa Selic, sem taxas de manutenção. |
| Perdi meu cartão, o que fazer? | Bloqueie o cartão imediatamente pelo aplicativo, na seção "Cartões" > "Bloquear cartão". Se precisar de um novo, solicite a segunda via pelo mesmo menu. |

## 2. Produtos financeiros

| Produto | Descrição simples | Observação |
|---|---|---|
| Poupança | Rendimento simples, sem taxas, liquidez diária | Baixo rendimento comparado a outros investimentos |
| CDB | Rende mais que a poupança, prazo definido, protegido pelo FGC até o limite legal | Pode ter liquidez diária ou apenas no vencimento, dependendo do CDB |
| Cartão de crédito | Permite parcelar compras e pagar em data futura | Juros altos em caso de atraso ou parcelamento da fatura |
| Empréstimo pessoal | Valor liberado à vista, pago em parcelas fixas | Taxa de juros varia conforme perfil e prazo |

## 3. Fórmulas de cálculo (uso demonstrativo)

> Todas as simulações usam taxas fictícias definidas neste arquivo, apenas para fins didáticos do protótipo.

- **Juros simples:** `M = C × (1 + i × t)`
  - C = capital inicial, i = taxa mensal (fictícia: 1% = 0.01), t = tempo em meses
- **Juros compostos:** `M = C × (1 + i) ^ t`
  - Mesma taxa fictícia de 1% ao mês, usada apenas para fins de demonstração
- **Financiamento simples (parcelas fixas, sem juros):** `Parcela = Valor total ÷ Número de parcelas`
  - Usado apenas para simulações sem juros embutidos (parcelamento simples)

## 4. Regras de uso da base

- A Vera **só** pode responder com base nas informações acima.
- Se a pergunta não tiver relação com nenhum item da base, a Vera deve dizer que não tem informação suficiente e sugerir contato com o atendimento humano.
- Taxas de juros usadas nos cálculos são **fictícias e apenas demonstrativas** — a Vera deve deixar isso explícito sempre que fizer uma simulação.
