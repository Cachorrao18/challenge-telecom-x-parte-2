
# 📊 Desafio Telecom X - Parte 2: Análise de Evasão de Clientes

Este projeto faz parte do Oracle Next Education (ONE) em parceria com a Alura, onde o desafio é analisar e prever a **evasão de clientes de uma empresa de telecomunicações**.

---

## 📥 Como subir este projeto no Google Colab

### 1. Acesse o Google Colab
- Acesse: [https://colab.research.google.com](https://colab.research.google.com)

### 2. Faça upload do notebook e do CSV
- Clique em **"Arquivo > Upload de notebook"** e envie o arquivo `Challenge_Telecom_X_análise_de_evasão_de_clientes_Parte_2.ipynb`
- Em seguida, execute a célula abaixo para enviar o CSV tratado:

```python
from google.colab import files
uploaded = files.upload()
```

- Selecione o arquivo `telecom_users_tratado.csv` do seu computador.
- Após o upload, carregue os dados com:

```python
import pandas as pd
df = pd.read_csv('telecom_users_tratado.csv')
```

---

## ✅ O que foi feito nos dados

1. **Remoção de colunas irrelevantes**  
   - Foi removida a coluna `customerID`, que não contribui para os modelos preditivos.

2. **Tratamento de valores nulos**  
   - Valores nulos foram excluídos ou convertidos corretamente, como no campo `TotalGasto`.

3. **Conversão de dados categóricos**  
   - Utilizamos o `One-Hot Encoding` para transformar variáveis como `Sexo`, `Serviços`, `TipoContrato` etc. em colunas numéricas.

4. **Análise de balanceamento**  
   - Verificamos a proporção de clientes que evadiram e os que permaneceram.

5. **Visualização da correlação entre variáveis**
   - Criamos uma matriz de correlação e gráficos de dispersão e boxplots para variáveis como `Tempo de contrato` e `Total gasto`.

6. **Modelagem com machine learning**
   - Usamos 2 modelos:
     - **Regressão Logística** (com normalização)
     - **Random Forest** (sem normalização)

7. **Avaliação dos modelos**
   - Foram utilizadas as métricas: acurácia, precisão, recall, F1-score e matriz de confusão.

8. **Análise de variáveis mais relevantes**
   - A importância das variáveis foi analisada em cada modelo para identificar fatores que influenciam a evasão.

---

## 📌 Conclusão

- O modelo **Random Forest** teve o melhor desempenho, com maior precisão e recall.
- Variáveis como **Tipo de Contrato**, **Fatura Eletrônica**, **Serviços Adicionais** e **Total Gasto** estão fortemente associadas à evasão.
- Estratégias como oferecer **contratos mais longos com benefícios**, **programas de fidelidade** e **melhorar o suporte ao cliente** podem ajudar na **retenção de clientes**.

---

📁 Este projeto é uma excelente introdução à análise de dados com pandas, visualização com matplotlib/seaborn e machine learning com scikit-learn.

