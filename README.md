# EBAC Projeto Parceria: Análise Inadimplência Crédito

**Objetivo**: Prever default (16%) em cartões para fintechs BR (perdas R$40bi/ano).

## 1. Coleta Dados
- `credito.csv` baixado EBAC utils (10k registros reais-like).

## 2. Tratamento
- Duplicatas/extremos removidos.
- `limite_credito`, `valor_transacoes_12m`: vírgula BR → float.
- Final: 10.127 linhas | 16.07% default.

## 3. EDA Insights
| Grupo | Limite Méd | Trans 12m |
|-------|------------|-----------|
| Bom (0) | R$13k | R$2.5k |
| Mau (1) | R$11k | R$2.2k |

Corr default: limite=-0.15.

![Dist Default](dist_default.png)

![Limite Default](box_limite_default.png)

![Transações Default](box_transacoes_default.png)

![Heatmap Corr](heatmap_default.png)

## 4. Conclusão
Foco risco: baixo limite + poucas transações.

**Vinicius | EBAC | Fev/2026**
