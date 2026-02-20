# Análise de GPUs: Custo-benefício com benchmarks (Time Spy, OpenCL e Vulkan)

Este projeto compara o **custo-benefício de GPUs high-end** no mercado brasileiro usando **benchmarks sintéticos** (desempenho bruto) e preços coletados.  
O objetivo é responder: **qual GPU entrega mais desempenho bruto por real investido?**

📓 Notebook completo com código, tabelas e gráficos:  
👉 [analise_gpus_preco_performance.ipynb](https://colab.research.google.com/drive/1Z71KbuVUGgdkKJ5rv15v3sH9_Qo4MS5E)

---

## Dados utilizados (recorte)

| GPU | Preço (R$) | Time Spy (Graphics) | OpenCL | Vulkan |
|---|---:|---:|---:|---:|
| RTX 5070 | 4599 | 15731 | 187414 | 188712 |
| RTX 5070 Ti | 6999 | 48656 | 229140 | 228576 |
| RX 9070 XT | 4999 | 53403 | 179178 | 177395 |

> Os preços representam uma coleta pontual do mercado brasileiro. Os benchmarks foram coletados de fontes públicas e serão referenciados na seção **Fontes**.

---

## Metodologia

Para comparar custo-benefício entre GPUs de forma padronizada, foi criado um **Índice de Desempenho Bruto** com base em três benchmarks:
- **3DMark Time Spy (DX12 / Graphics Score)**
- **OpenCL**
- **Vulkan**

Como os testes possuem escalas diferentes, os scores foram **normalizados** (melhor resultado em cada teste = 100) e combinados em uma **média**.

### Métrica principal: Índice por R$ 1.000
**Índice por R$ 1.000 = (Índice de Desempenho Bruto / Preço) × 1000**

Quanto maior esse valor, **mais desempenho bruto o consumidor recebe por R$ 1.000 investidos**.

---

## Resultados

![Custo-benefício — Índice por R$ 1.000](images/indice_por_1000.png)

### Principais achados
- Considerando os preços coletados e os benchmarks utilizados, a **RX 9070 XT** apresentou o maior **Índice por R$ 1.000**, liderando em custo-benefício no cenário de **desempenho bruto**.
- A **RTX 5070 Ti**, apesar de alto desempenho absoluto, ficou atrás em custo-benefício no preço considerado.
- A **RTX 5070** ficou em posição inferior no índice agregado, indicando menor retorno de desempenho por real investido dentro deste recorte.

*Interpretação curta:* no recorte analisado, a RX 9070 XT entrega mais desempenho bruto por R$ 1.000 investidos.

---

## Limitações (importante)
Este projeto mede **desempenho bruto/sintético** e não considera tecnologias e otimizações em jogos como **DLSS/Frame Generation (NVIDIA)** e **FSR (AMD)**.  
Em jogos reais, os resultados podem variar conforme título, resolução e configurações.

---

## Contexto de mercado (referências)
- **Popularidade na base gamer (Steam):** a pesquisa mensal de hardware do Steam (jan/2026) indica participação aproximada de **NVIDIA ~73%**, **AMD ~18%** e **Intel ~8%**.
- **NVIDIA e foco em IA (contexto financeiro):** relatórios financeiros recentes mostram receita de **Data Center** muito maior do que **Gaming**, o que ajuda a explicar a relevância do mercado de IA no negócio atual da empresa.  
  *Observação:* isso não prova mudanças diretas em produtos, mas dá contexto de mercado.

---

## Fontes
- (https://www.3dmark.com/ https://browser.geekbench.com/)
- Steam Hardware Survey (jan/2026): (link)
- Relatório financeiro NVIDIA (Q3 FY2026): (link)
- Benchmarks (Time Spy/OpenCL/Vulkan): (link)
- Preços (lojas/data da coleta): (link)

---
