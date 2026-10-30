# Dashboard de Vendas e Estoque

## 1. Visão geral

Projeto de análise de dados desenvolvido para demonstrar uma solução de Business Intelligence voltada ao acompanhamento de vendas, desempenho de produtos e gestão de estoques.

O objetivo é transformar dados transacionais em indicadores que auxiliem a tomada de decisões comerciais e o planejamento de reposição de mercadorias.

### Tecnologias utilizadas

- **Python:** Pandas e NumPy para tratamento, transformação e validação dos dados.
- **Power BI:** modelagem, medidas DAX e construção de dashboards interativos.
- **Jupyter Notebook:** organização e execução das etapas de preparação dos dados.
- **CSV:** armazenamento e intercâmbio dos conjuntos de dados.

## 2. Fonte dos dados

O projeto utiliza uma versão pública do conjunto de dados *Sample Superstore*, contendo registros de vendas de uma empresa fictícia.

**Características da base:**

- 9.800 registros de vendas.
- 4.922 pedidos distintos.
- Período de 2015 a 2018.
- 793 clientes.
- 1.893 produtos identificados após o tratamento das inconsistências cadastrais.

Os dados de estoque foram simulados para fins educacionais e de demonstração.

## 3. Tratamento e qualidade dos dados

O tratamento foi realizado em Python, utilizando principalmente a biblioteca Pandas.

As principais atividades foram:

- Verificação de valores ausentes e registros duplicados.
- Padronização dos tipos de dados e das datas.
- Identificação de inconsistências nos valores monetários.
- Reconciliação dos valores de vendas com uma base pública de referência.
- Tratamento de códigos de produtos associados a nomes diferentes.
- Criação de identificadores substitutos para produtos.
- Validação dos totais e dos relacionamentos.

Após o tratamento, o faturamento total validado foi de **2.261.536,78**, nas unidades monetárias da base de origem.

## 4. Modelagem dimensional

Foi desenvolvido um modelo dimensional com tabelas de fatos e dimensões.

**Dimensões:**

- Dim_Produtos
- Dim_Clientes
- Dim_Calendario
- Dim_Localizacao

**Tabelas de fatos:**

- Fato_Vendas
- Fato_Estoque

O modelo utiliza chaves para relacionar as tabelas e permitir análises por produto, cliente, período e localização.

A tabela Fato_Estoque representa uma fotografia simulada do estoque, não um histórico de movimentações.

## 5. Indicadores e análises

### Análise de vendas

- Faturamento total.
- Quantidade de pedidos.
- Ticket médio.
- Crescimento anual (YoY).
- Evolução mensal do faturamento.
- Faturamento por categoria.

### Análise de produtos

- Ranking dos dez produtos com maior faturamento.
- Faturamento por subcategoria.
- Participação das categorias no faturamento.
- Quantidade de produtos comercializados.
- Faturamento médio por produto.
- Classificação ABC baseada no faturamento acumulado de 2015 a 2018.

### Gestão de estoque

- Valor total do estoque simulado.
- Quantidade de produtos críticos.
- Produtos abaixo do mínimo e sem estoque.
- Necessidade de reposição mínima.
- Quantidade de compra sugerida.
- Custo de reposição e investimento estimado.
- Priorização de produtos críticos por classe ABC.

## 6. Resultados

O dashboard permite explorar o desempenho comercial, identificar produtos de maior relevância financeira e consultar necessidades simuladas de reposição.

**Resultados históricos de vendas:**

- Faturamento total: 2.261.536,78.
- Pedidos distintos: 4.922.
- Ticket médio: 459,48.
- Produtos identificados: 1.893.

**Resultados da simulação de estoque:**

- Produtos críticos: 157.
- Unidades para reposição mínima: 1.766.
- Unidades de compra sugerida: 8.366.
- Investimento estimado para compra sugerida: 1.993.248,63.

## 7. Limitações e melhorias futuras

- O conjunto de dados é público e representa operações fictícias.
- O estoque é simulado e não representa saldos reais de uma empresa.
- Não existem quantidades efetivamente vendidas por item na base original.
- A classificação ABC é histórica e não se recalcula automaticamente conforme o período selecionado.
- Os custos de estoque e reposição são estimativas da simulação.
- O projeto pode ser expandido com dados reais de compras, fornecedores, movimentações e prazos de entrega.
- Uma evolução futura seria implementar atualização automatizada dos dados e indicadores de giro e cobertura de estoque.