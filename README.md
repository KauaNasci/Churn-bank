
---

# 📊 Previsão de Churn Bancário com Machine Learning

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)

## 📌 Visão Geral do Projeto
Este projeto foi desenvolvido para prever a rotatividade de clientes (**Churn**) em uma instituição bancária. O objetivo principal é identificar padrões que levam um cliente a cancelar seus serviços, permitindo que a empresa tome ações preventivas baseadas em dados.

O modelo utiliza o algoritmo **Random Forest** e aplica técnicas avançadas para lidar com o desbalanceamento de classes, garantindo uma previsão realista e útil para o negócio.

---

## 🛠️ Tecnologias e Ferramentas
*   **Linguagem:** Python.
*   **Manipulação de Dados:** Pandas e NumPy.
*   **Visualização:** Seaborn e Matplotlib.
*   **Machine Learning:** Scikit-Learn.
*   **Persistência do Modelo:** Joblib.

---

## 🚀 Pipeline do Projeto

### 1. Limpeza e Engenharia de Dados
*   Remoção de identificadores irrelevantes (`RowNumber`, `CustomerId`, `Surname`) para evitar *overfitting*.
*   Transformação de variáveis categóricas em numéricas utilizando `LabelEncoder`.
*   Separação rigorosa de variáveis de comportamento vs. variáveis de resultado.

### 2. Tratamento de Desbalanceamento
Em cenários de Churn, o número de clientes que saem é muito menor que os que ficam. Para evitar um modelo tendencioso, utilizei a estratégia `class_weight='balanced'`, que ajusta o peso das classes durante o treinamento do **Random Forest**.

### 3. Resultados e Métricas
O modelo foi avaliado com foco na **Acurácia Balanceada**, que reflete melhor o desempenho em dados desiguais:
*   **Acurácia Geral:** 86.30%.
*   **Acurácia Balanceada:** 70.98%.

---

## 📈 Insights Principais
A análise de **Feature Importance** revelou que os fatores determinantes para o Churn são:
1.  **Idade:** Clientes em determinadas faixas etárias apresentam maior propensão à saída.
2.  **Saldo Bancário:** O volume de capital mantido influencia diretamente a retenção.
3.  **Número de Produtos:** Clientes com menos produtos ativos possuem maior risco de evasão.

---

## 📂 Como Utilizar
1.  Clone o repositório.
2.  Instale as dependências: `pip install -r requirements.txt`.
3.  Execute o notebook ou carregue o modelo salvo:
    ```python
    import joblib
    modelo = joblib.load('modelo_churn_bancario.pkl')
    ```

---

## 👨‍💻 Autor
**Francisco Kauã do Nascimento Barros**
*   Estudante de Tecnologia em Ciência de Dados (UNINTER).
*   Técnico em Desenvolvimento de Sistemas.
*   Especialista em Automação
  
**Nota:** Este projeto faz parte do meu portfólio de estudos em Machine Learning e análise preditiva aplicados ao setor financeiro.
