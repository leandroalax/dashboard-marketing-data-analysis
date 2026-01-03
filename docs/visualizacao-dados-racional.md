# Visualização de Dados Racional

Este documento descreve o racional por trás da escolha de cada visualização utilizada no **Dashboard de Análise de Campanhas de Marketing**, garantindo clareza, coerência analítica e alinhamento com os objetivos exploratórios.

---

## 1. Visão Cliente

### Cartões de KPI

<img width="1227" height="216" alt="print - kpi cards" src="https://github.com/user-attachments/assets/39c21a00-defe-4774-a7a9-8e933caa425d" />

**Objetivo:** Apresentar uma visão geral e imediata do dataset.

* Total de Clientes
* Salário Anual Médio
* Total de Compras por Canal (Loja, Web, Catálogo)
* Total de Compras com Desconto
* Etc.

**Racional:** Os KPIs permitem que gestores compreendam rapidamente a dimensão da base de clientes e a relevância de cada canal antes de análises mais profundas.

---

### Gráficos de Barras – Escolaridade e Estado Civil

<img width="1221" height="261" alt="print - bars grafic_educacion lvl e marital status " src="https://github.com/user-attachments/assets/b1fa8e09-77cb-48b9-84ff-32b8dfd83e63" />

**Objetivo:** Entender a distribuição dos clientes por características demográficas.

**Racional:** Gráficos de barras são ideais para comparações categóricas, facilitando a identificação de grupos predominantes e segmentos estratégicos.

---

## 2. Comportamento de Compra do Cliente

<img width="601" height="312" alt="print - scatter plot_spend x income" src="https://github.com/user-attachments/assets/3012b165-59a6-4f86-876b-5770fc261b4c" />

### Gráfico de Dispersão – Total Gasto x Salário Anual

**Objetivo:** Identificar correlações entre renda e nível de gasto.

**Racional:** Gráficos de dispersão permitem observar padrões, clusters e possíveis outliers, sendo essenciais em análises exploratórias.

---

### Árvore de Decomposição – Total Gasto por Estado Civil e Escolaridade

<img width="622" height="302" alt="print - decomposition tree_spend by marital by country" src="https://github.com/user-attachments/assets/087c9769-21f3-4c8b-a218-abe121777d74" />

**Objetivo:** Detalhar a contribuição de segmentos demográficos no gasto total.

**Racional:** A árvore de decomposição possibilita análises interativas e hierárquicas, favorecendo a identificação de segmentos mais rentáveis.

---

### Gráficos de Barras – Composição Familiar

<img width="1225" height="281" alt="print - bar graffic_household composition" src="https://github.com/user-attachments/assets/08cf536f-cc1e-49b4-9ec6-b452738eed77" />

**Objetivo:** Avaliar o impacto de filhos e adolescentes no comportamento de compra.

**Racional:** A simplicidade dos gráficos de barras facilita a comparação direta entre diferentes perfis familiares.

---

## 3. Performance das Campanhas de Marketing

### Gráfico de Barras Empilhadas – Efetividade x Número de Filhos

<img width="708" height="285" alt="print - bar chart_campaing effectiv and n  Children" src="https://github.com/user-attachments/assets/e5e1730e-b61b-4f3d-9fd8-6f552ceb322b" />

**Objetivo:** Avaliar a resposta às campanhas considerando a composição familiar.

**Racional:** Barras empilhadas permitem comparar resultados preservando a proporção entre respostas positivas e negativas.

---

### Gráfico de Pizza – Resultado das Campanhas

<img width="487" height="285" alt="print - pie chart_campaing results" src="https://github.com/user-attachments/assets/35edc5eb-6c06-4743-a109-80e32438747e" />

**Objetivo:** Demonstrar a taxa geral de conversão.

**Racional:** Gráficos de pizza são adequados para representar relações parte-todo de forma rápida e intuitiva.

---

### Matriz e Gráfico de Barras – Escolaridade, Estado Civil e Resultado

<img width="1212" height="290" alt="print - matrix and bar chart_education marital and campaing results" src="https://github.com/user-attachments/assets/46d70dab-3f20-4959-8abd-ed78249eca0f" />

**Objetivo:** Análise detalhada por segmentação.

**Racional:** Tabelas garantem precisão analítica, enquanto gráficos de barras facilitam a interpretação visual das diferenças de renda entre clientes que compraram e não compraram.

---

## 4. Padrões de Compra por Ponto de Venda

### Gráfico Combinado (Colunas e Linha) – Gasto por Categoria e País

<img width="1207" height="297" alt="print - column and line chart_spend by category and country" src="https://github.com/user-attachments/assets/5f1a568a-6898-4ccb-8c4e-5143ba72af30" />

**Objetivo:** Comparar gastos por categoria considerando o volume de clientes.

**Racional:** A combinação de colunas e linha permite analisar simultaneamente valor financeiro e tamanho da base de clientes por país.

---

### Gráfico de Linhas – Evolução do Gasto por Ano e País

<img width="1205" height="288" alt="print - line chart_spend by country and year" src="https://github.com/user-attachments/assets/bce75a19-b7b1-4b40-bfb9-26e96afced5d" />

**Objetivo:** Analisar tendências temporais de consumo.

**Racional:** Gráficos de linhas são os mais adequados para séries temporais, evidenciando tendências, picos e quedas.

---
