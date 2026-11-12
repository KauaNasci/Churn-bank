# 📊 Previsão de Churn Bancário com Machine Learning

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

## 📌 Visão Geral do Projeto
Este projeto foi desenvolvido para prever a rotatividade de clientes (**Churn**) em uma instituição bancária. O objetivo principal é identificar padrões que levam um cliente a cancelar seus serviços, permitindo que a empresa tome ações preventivas baseadas em dados.

O modelo utiliza o algoritmo **Random Forest** e aplica técnicas para lidar com o desbalanceamento de classes, garantindo uma previsão realista e útil para a tomada de decisão do negócio.

---

## 🛠️ Tecnologias e Ferramentas
* **Linguagem:** Python
* **Manipulação e Qualidade de Dados:** Pandas e NumPy
* **Visualização:** Seaborn e Matplotlib
* **Machine Learning:** Scikit-Learn
* **Persistência do Modelo:** Joblib

---

## 🚀 Pipeline do Projeto

### 1. Limpeza e Engenharia de Dados
* Remoção de identificadores únicos (`RowNumber`, `CustomerId`, `Surname`) para evitar ruído e vazamento de identificação nos dados.
* Transformação de variáveis categóricas em numéricas utilizando `LabelEncoder`.
* Separação rigorosa entre variáveis explicativas (comportamento) e variável alvo (resultado), prevenindo *data leakage*.

### 2. Tratamento de Desbalanceamento
Em cenários de Churn, o volume de clientes que cancelam o serviço é muito menor do que o de clientes retidos. Para evitar um modelo enviesado para a classe majoritária, utilizei a estratégia `class_weight='balanced'`, que ajusta automaticamente o peso das classes durante o treinamento do **Random Forest**.

### 3. Resultados e Métricas
O modelo foi avaliado com foco na **Acurácia Balanceada**, métrica mais adequada para refletir o desempenho real em bases desiguais:
* **Acurácia Geral:** 86,30%
* **Acurácia Balanceada:** 70,98%

---

## 📈 Insights Principais
A análise de **Feature Importance** revelou que os fatores determinantes para o Churn são:
1. **Idade:** Clientes em determinadas faixas etárias apresentam maior propensão à saída.
2. **Saldo Bancário:** O volume de capital mantido influencia diretamente a retenção.
3. **Número de Produtos:** Clientes com menos produtos ativos possuem maior risco de evasão.

---

## 📂 Como Utilizar
1. Clone o repositório:
   ```bash
   git clone https://github.com
   ```
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Execute o notebook `Churn_bancário.ipynb` ou carregue o modelo salvo:
   ```python
   import joblib
   modelo = joblib.load('modelo_churn_bancario.pkl')
   ```

---

## 👨‍💻 Autor
**Francisco Kauã do Nascimento Barros**
* Estudante de Tecnologia em Ciência de Dados (UNINTER)
* Técnico em Desenvolvimento de Sistemas
* Foco em Analytics Engineering, SQL e Engenharia de Dados
* [![LinkedIn](https://shields.io)](https://linkedin.com)

**Nota:** Este projeto faz parte do meu portfólio de estudos em engenharia de atributos, preparação de dados e modelagem preditiva aplicados ao setor financeiro.
