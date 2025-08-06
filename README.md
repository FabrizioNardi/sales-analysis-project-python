# 🛍️ Sales Analysis & Binary Classification with Keras

Este projeto realiza uma análise exploratória de vendas e aplica um modelo de Machine Learning para prever um resultado binário com base em dados comerciais e demográficos. O objetivo é explorar padrões nos dados e utilizar inteligência artificial para auxiliar em decisões estratégicas.

---

## 📁 Dados Utilizados

O conjunto de dados foi extraído de um arquivo Excel com múltiplas planilhas:

- **clientes**: ID, nome, sexo, data de nascimento
- **lojas**: localização das lojas
- **produtos**: descrição e valor unitário
- **vendas**: ID do cliente, produto, loja, data da venda
- **pagamentos**: forma e data de pagamento

---

## 🧹 Etapas de Preparação dos Dados

- Detecção e tratamento de valores nulos
- Conversão de datas e cálculo da idade dos clientes
- Unificação dos dados em um único dataframe
- Codificação de variáveis categóricas (`get_dummies`, `LabelEncoder`)
- Normalização dos dados com `StandardScaler`

---

## 📊 Análise Exploratória

- Distribuição de idade dos clientes
- Frequência de vendas por loja
- Produtos mais vendidos
- Correlação entre idade, forma de pagamento e valor de venda
- Visualizações usando `matplotlib` e `seaborn`

---

## 🤖 Machine Learning

Um modelo de classificação binária foi desenvolvido utilizando **Keras (TensorFlow backend)**.

### 🔧 Estrutura do Modelo

- **Modelo**: `Sequential`
- **Camadas**:
  - Dense(15, activation='relu')
  - Dense(7, activation='relu')
  - Dense(3, activation='relu')
  - Dense(1, activation='sigmoid')
- **Função de perda**: `binary_crossentropy`
- **Métrica**: `accuracy`
- **Otimizador**: `Adam`
- **Batch size**: 128
- **Épocas**: 300
- **Divisão treino/teste**: 90% / 10%

### 📈 Resultados

- **Acurácia obtida**: **83%** no conjunto de teste
- Convergência clara nos gráficos de `loss` e `accuracy`
- Boa separação entre as classes alvo

> O modelo prevê com 83% de precisão o comportamento binário de vendas com base em variáveis como idade, valor da compra e características do cliente/produto.

---

## 📌 Próximos Passos

- Avaliação com matriz de confusão, precisão, recall e F1-score
- Aplicação de validação cruzada (ex: `StratifiedKFold`)
- Otimização de hiperparâmetros
- Deploy via API (Flask ou FastAPI)
- Interpretação com SHAP ou LIME

---

## 🛠️ Tecnologias Utilizadas

- Python
- Pandas & NumPy
- Matplotlib & Seaborn
- Scikit-learn
- TensorFlow / Keras

---

## 👤 Autor

**Fabrizio Brun Nardi**  
📍 Porto Alegre – RS  
📧 fabrizionardi5@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/fabrizionardi5) | [GitHub](https://github.com/fabrizionardi5)

---

