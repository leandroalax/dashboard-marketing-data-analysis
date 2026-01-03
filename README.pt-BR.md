### Visão Geral do Projeto

Este projeto apresenta um dashboard analítico voltado à **análise de campanhas de marketing e comportamento dos clientes**. A solução foi desenvolvida em **Microsoft Power BI**, com o objetivo de transformar dados brutos em insights acionáveis para apoiar a tomada de decisão.

O projeto foi desenvolvido como parte do **Mini-Projeto I – Capítulo 4** do programa *Microsoft Power BI para Business Intelligence e Data Science* da **Data Science Academy (DSA)**.

Diferentemente de cenários tradicionais, o cliente não forneceu perguntas de negócio bem definidas. Assim, a análise seguiu uma abordagem **exploratória e diagnóstica**, buscando identificar padrões relevantes relacionados ao perfil dos clientes, comportamento de compra, canais e efetividade das campanhas.

---

### Descrição do Dataset

Foi disponibilizado um único dataset em formato CSV, contendo aproximadamente **2.000 registros**, sem dados nulos ou em branco.

**Principais atributos:**

* Dados demográficos dos clientes (ano de nascimento, escolaridade, estado civil, país)
* Composição familiar (filhos e adolescentes em casa)
* Salário anual
* Gastos por categoria de produto
* Canais de compra (loja, web, catálogo)
* Participação e resultados das campanhas

---

### Tratamento dos Dados

Durante a etapa de exploração, foram identificados **outliers em variáveis numéricas**. Após validação com o contexto de negócio, esses valores foram classificados como **erros de preenchimento** e removidos.

Para consolidar o gasto total por cliente, foi criada a seguinte medida em DAX:

```DAX
Total Gasto =
SUMX(
    DadosMarketing,
    DadosMarketing[Gasto com Alimentos]
    + DadosMarketing[Gasto com Brinquedos]
    + DadosMarketing[Gasto com Eletronicos]
    + DadosMarketing[Gasto com Moveis]
    + DadosMarketing[Gasto com Utilidades]
    + DadosMarketing[Gasto com Vestuario]
)
```

Também foi realizada a padronização da feature **"Comprou"**, substituindo os valores 0 e 1 por **"Não"** e **"Sim"**, facilitando a interpretação.

---

### Estrutura do Dashboard

O dashboard está organizado em quatro visões analíticas:

1. **Visão Cliente** – Perfil demográfico e canais de compra.
<img width="1231" height="698" alt="Print - Visão Cliente" src="https://github.com/user-attachments/assets/87d42efc-ce82-4d96-a977-a5bbc4596fc7" />

2. **Visão Comportamento de Compra** – Relação entre renda, composição familiar e gasto total.
<img width="1233" height="687" alt="Print - Visão Comportamento de Compra do Cliente" src="https://github.com/user-attachments/assets/da57be01-4ce6-40b1-9a7a-4b22b0887e11" />

3. **Visão da Performance das Campanhas de Marketing** – Análise de efetividade e resposta dos clientes.
<img width="1230" height="687" alt="Print - Visão Performance das Campanhas de Marketing" src="https://github.com/user-attachments/assets/efe9b0ce-3072-40fe-8862-18cf09a2ebe5" />

4. **Visão de Padrões de Compra por Ponto de Venda** – Distribuição de gastos por país, categoria e tempo.
<img width="1227" height="687" alt="Print - Visão de Padrões de Compra por Ponto de Venda" src="https://github.com/user-attachments/assets/4e177e4a-ef95-4a5d-bbe7-457a3d87bbef" />


Para uma explicação detalhada da lógica das visualizações, consulte:  
📄 [Lógica de Visualização de Dados](docs/visualizacao-dados-racional.md)
---

### Ferramentas Utilizadas

* Microsoft Power BI
* DAX
* Dataset em formato CSV

---
### Principais Conclusões e Insights de Negócio

Com base na análise exploratória dos dados e nos dashboards desenvolvidos, foram identificados os seguintes insights relevantes:

* Concentração do Perfil de Clientes
A base de clientes é majoritariamente composta por indivíduos com níveis mais elevados de escolaridade, especialmente ensino superior e pós-graduação. Isso indica um público com maior poder aquisitivo e maior propensão a responder a estratégias de marketing orientadas a valor.

* Estado Civil e Comportamento de Compra
Clientes solteiros representam a maior parcela da base e concentram o maior volume de gastos. Esse perfil se mostra estratégico para ações de marketing mais personalizadas e com maior potencial de retorno.

* Relação entre Renda e Gasto
Observa-se uma correlação positiva entre salário anual e gasto total, embora com redução do ganho marginal em faixas salariais mais altas. Isso evidencia que outros fatores — como estilo de vida e composição familiar — influenciam diretamente o comportamento de compra.

* Impacto da Composição Familiar
Clientes sem filhos ou adolescentes em casa apresentam gasto total significativamente maior. À medida que o número de dependentes aumenta, o gasto tende a diminuir, indicando restrições orçamentárias ou mudança nas prioridades de consumo.

* Desempenho Geográfico e por Canal
Os Estados Unidos lideram de forma consistente o gasto total por categoria e ao longo dos anos, seguidos por Espanha e Chile. As lojas físicas permanecem como o principal canal de compra, enquanto os canais digitais apresentam oportunidade de expansão com estratégias direcionadas.

* Efetividade das Campanhas de Marketing
A maior parte dos clientes não realizou compras durante as campanhas. No entanto, os clientes que converteram possuem, em média, salários anuais mais elevados, indicando que renda é um fator determinante para o sucesso das campanhas.

* Implicação de Negócio:
Os resultados indicam que as estratégias de marketing devem priorizar clientes de maior renda, solteiros e sem filhos, além de investir em segmentação mais refinada para aumentar a taxa de conversão nos demais perfis.

---

### Author

**Leandro Álax**
Data Analytics | Business Intelligence | Power BI

Para consultas profissionais ou oportunidades de colaboração,
leandroalax@hotmail.com
