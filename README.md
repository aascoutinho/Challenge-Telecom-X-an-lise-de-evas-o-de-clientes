
# 📊 Análise de Evasão de Clientes (Churn) - Telecom X

Este projeto realiza uma análise exploratória (EDA) dos dados de clientes da empresa **Telecom X**, com o objetivo de identificar os fatores que influenciam a evasão (churn). A análise aplica o processo completo de **ETL** (Extração, Transformação e Carga), visualizações e insights estratégicos que servirão de base para modelos preditivos de retenção.

---

## 🧠 Objetivo

> Identificar padrões de comportamento e características associadas a clientes que cancelaram os serviços da Telecom X, possibilitando ações preventivas e estratégias de retenção por parte da equipe de Data Science.

---

## 🔄 Processo ETL

### 🔹 Extração
- Fonte: JSON hospedado no GitHub.
- URL:  
  `https://raw.githubusercontent.com/ingridcristh/challenge2-data-science/main/TelecomX_Data.json`
- Acesso via biblioteca `requests` para importar dados diretamente da web.

### 🔹 Transformação
- Conversão para `DataFrame` com **pandas**.
- Expansão de colunas aninhadas (`customer`, `phone`, `internet`, `account`).
- Criação das colunas `Charges_Monthly` e `Charges_Total`.
- Conversão de tipos e limpeza de valores nulos.

### 🔹 Carga
- Dataset final com **7.256 registros** e **21 atributos tratados**, pronto para análise.

---

## 📊 Análise Exploratória (EDA)

A análise foi realizada com as bibliotecas:

- `pandas` – tratamento dos dados
- `matplotlib` e `seaborn` – visualização dos dados

### Principais descobertas:

| Fator                   | Insight Relevante |
|------------------------|-------------------|
| **Churn geral**        | 25,7% da base cancelou |
| **Tipo de contrato**   | Contratos mensais têm maior churn |
| **Tipo de internet**   | Fibra óptica apresenta maior evasão |
| **Tenure**             | Clientes que cancelam permanecem menos de 20 meses |
| **Gasto mensal**       | Gasto elevado tende a maior churn |
| **Forma de pagamento** | Electronic check possui churn acima da média |

---

## 📈 Visualizações

O projeto inclui gráficos como:

- 📊 Gráficos de barras (absoluto e percentual)
- 📦 Boxplots para comparação de métricas contínuas (tenure, gasto)
- 🔥 Heatmap de correlação

---

## 📌 Recomendações

1. Desenvolver modelos preditivos com foco em:
   - Contratos mensais
   - Clientes com fibra óptica
   - Método de pagamento Electronic Check

2. Criar estratégias de **retenção**:
   - Campanhas de fidelização para os primeiros 24 meses
   - Incentivar uso de meios de pagamento mais estáveis

3. Implementar **alertas de churn**:
   - Notificações para ações comerciais preventivas

---

## 🧾 Relatório Final

📄 O relatório em PDF pode ser acessado aqui:  
👉 [Relatório_Churn_TelecomX.pdf](Relatorio_Churn_TelecomX.pdf)

---

## ▶️ Como Executar

1. Clone o repositório ou baixe os arquivos do projeto.
2. Instale as dependências com:

```bash
pip install pandas matplotlib seaborn requests fpdf
```

3. Execute o script principal:

```bash
python telecomX.py
```

---

## 🛠️ Tecnologias Utilizadas

- Python 3.11
- pandas
- matplotlib
- seaborn
- requests
- fpdf (para geração de PDF)

---

## 🧪 Próximos Passos

- Implementação de modelos preditivos (ex: Random Forest, XGBoost)
- Dashboard interativo com Plotly/Dash
- Integração com banco de dados ou API real de clientes

---
