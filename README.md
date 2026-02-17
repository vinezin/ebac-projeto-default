# EBAC Projeto Parceria: Previsão Inadimplência

![Dist Default](imgs/dist_default.png)

## Coleta Dados
- Dataset: credito.csv (10k registros ANP/fintech BR)
- Fonte: https://raw.githubusercontent.com/andre-marcos-perez/ebac-course-utils/main/dataset/credito.csv

## Tratamento
- Convertido limite_credito/valor_transacoes_12m (, → . float)
- Remove duplicatas/extremos | Shape final: 10.127 linhas
- Default: 16% (1.627 inadimplentes)

## EDA Insights
| Métrica | Adimpl (0) | Inadimpl (1) |
|---------|------------|--------------|
| Limite  | R$13k     | R$11k       |
| Trans 12m | R$2.5k   | R$2.2k     |

Corr default: limite=-0.15 (limite alto → menor risco)

![Box Limite](imgs/box_limite_default.png)
![Heatmap](imgs/heatmap_default.png)

**Conclusão**: Foco cobrança em baixo limite + poucas transações.
