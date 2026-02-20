# Meu Primeiro Projeto de Dados

Este é meu primeiro projeto de análise de dados usando Python.

## Resultados

### Métrica principal: Índice por R$ 1.000
Para comparar custo-benefício entre GPUs de forma padronizada, foi criado um **Índice de Desempenho Bruto** com base em três benchmarks (Time Spy DX12, OpenCL e Vulkan). Como os testes possuem escalas diferentes, os scores foram normalizados (melhor resultado em cada teste = 100) e combinados em uma média.

A métrica usada para custo-benefício foi:

**Índice por R$ 1.000 = (Índice de Desempenho Bruto / Preço) × 1000**

Quanto maior esse valor, **mais desempenho bruto o consumidor recebe por R$ 1.000 investidos**.

### Principais achados
- Considerando os preços coletados e os benchmarks utilizados, a **RX 9070 XT** apresentou o maior **Índice por R$ 1.000**, liderando em custo-benefício no cenário de **desempenho bruto**.
- A **RTX 5070 Ti**, apesar de alto desempenho, ficou atrás em custo-benefício no preço considerado.
- A **RTX 5070** ficou em posição inferior no índice agregado, indicando menor retorno de desempenho por real investido dentro deste recorte.

> Observação: este projeto mede **desempenho bruto/sintético** e não considera tecnologias e otimizações em jogos como **DLSS/Frame Generation (NVIDIA)** e **FSR (AMD)**. Em jogos reais, os resultados podem variar conforme título, resolução e configurações.
> ![Custo-benefício — Índice por R$ 1.000](images/indice_por_1000.png)
