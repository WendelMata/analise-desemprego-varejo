# 📊 Análise Econômica — Desemprego e Varejo (IBGE)

## 🔎 Visão Geral
Este projeto realiza uma **análise integrada entre o mercado de trabalho e o desempenho do varejo brasileiro (2020–2025)**, utilizando uma **arquitetura em camadas (Medallion)** no **Databricks** e visualização final no **Power BI**.

O objetivo é compreender **como o consumo e o desemprego se relacionam ao longo do tempo**, especialmente durante e após o impacto da **pandemia de COVID-19**.

---

## ⚙️ Tecnologias Utilizadas
- **Databricks (PySpark)** → Ingestão e tratamento dos dados.  
- **Arquitetura Medallion (Bronze / Silver / Gold)** → Organização e limpeza progressiva dos dados.  
- **Power BI** → Visualização e criação de dashboards interativos.  
- **IBGE API** → Fonte oficial de dados (taxa de desocupação e volume de vendas no varejo).  
- **Git & GitHub** → Versionamento e publicação do projeto.

---

## 🧱 Pipeline ETL — Arquitetura Medallion

O projeto segue o padrão **Medallion Architecture**, dividido em três camadas principais:

### 🥉 Bronze (Ingestão)
- Coleta de dados diretamente da **API pública do IBGE** (Taxa de Desocupação e Volume de Vendas no Varejo).  
- Dados armazenados **sem transformações**, garantindo integridade das informações originais.  
- Representa a **fonte bruta**, essencial para rastreabilidade e auditoria.  

### 🥈 Silver (Transformação)
- Limpeza e padronização dos datasets (nomes, tipos de dados e datas).  
- Mesclagem entre séries históricas de desemprego e varejo.  
- Criação de campos derivados, como **variação mensal (%)** e **médias móveis trimestrais (MA3)**.  
- Base usada para análises e integração com o Power BI.  

### 🥇 Gold (Curadoria)
- Consolidação e cálculo das **métricas finais**.  
- Envio dos dados finais ao **Power BI**, com dashboards que exploram a relação entre **consumo e emprego**.  
- Entrega valor analítico ao usuário final via dashboards e insights.  

---

## 📈 Resultados e Conclusões

A análise revelou uma **relação positiva, embora moderada, entre o consumo no varejo e a taxa de desemprego** no Brasil entre 2020 e 2025.

Durante a **pandemia de COVID-19**, observou-se um forte impacto sobre o comércio e o mercado de trabalho:
- Em **2020 e 2021**, o varejo apresentou **oscilações acentuadas**, impulsionado por medidas de restrição e posterior reabertura.  
- A **taxa de desemprego**, por outro lado, **demorou mais a reagir**, refletindo o tempo necessário para reabsorção da força de trabalho.  

Em anos posteriores, o cenário mostrou que **melhoras no varejo tendem a anteceder reduções na taxa de desemprego**, ainda que com defasagem temporal.  
Isso reforça o papel do **consumo como um dos primeiros indicadores de recuperação econômica**.  

> 💡 **Síntese:**  
> Quando o consumo cresce, o emprego tende a melhorar nos meses seguintes — o varejo reage rápido, mas o mercado de trabalho precisa de mais tempo para acompanhar.

---

## 🖼️ Exemplos Visuais

### 📊 Página 1 — Análise Econômica (Desemprego e Varejo)
![Dashboard Página 1](./docs/dashboard_pagina1.png)

### 📈 Página 2 — Resumo e Conclusões
![Dashboard Página 2](./docs/dashboard_pagina2.png)

---

## 🤝 Créditos e Contatos
**Autor:** [Wendel Mata](https://www.linkedin.com/in/wendel-mata-b31633206/)  
📍 **Ferramentas:** Databricks | PySpark | Power BI | IBGE API  
📂 **Repositório:** [github.com/WendelMata/analise-desemprego-varejo](https://github.com/WendelMata/analise-desemprego-varejo)

---
⭐ *Se este projeto foi útil, deixe uma estrela no repositório para apoiar futuras análises!*

