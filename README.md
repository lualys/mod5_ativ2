
# 🧠 Classificação de Vinhos com Aprendizado de Máquina

Este projeto tem como objetivo aplicar técnicas de **Aprendizado de Máquina** para classificar tipos de vinhos com base em suas características químicas. Utilizamos o dataset `load_wine` da biblioteca `sklearn.datasets`.

---

## 🎯 Objetivos

- Praticar a **exploração e preparação de dados**.
- Aplicar algoritmos de **classificação supervisionada**.
- Avaliar o desempenho dos modelos usando **métricas apropriadas** (Acurácia, Precisão, Recall, F1-score).
- (Opcional) Ajustar hiperparâmetros com **GridSearchCV**.

---

## 📦 Dataset

O conjunto de dados contém 178 amostras de vinhos, com 13 atributos químicos como:

- `alcohol`, `malic_acid`, `ash`, `flavanoids`, `color_intensity`, etc.
- A coluna `target` indica o tipo de vinho (0, 1 ou 2).

Dataset fornecido por:
```python
from sklearn.datasets import load_wine
```

---

## 🧪 Etapas do Projeto

### 1. Exploração dos Dados
- Visualização das primeiras linhas.
- Estatísticas descritivas (`mean`, `std`, `min`, `max`, etc.).
- Verificação de valores ausentes.
- Distribuição das classes (`target`).
- Análise de correlação entre variáveis com `heatmap`.
- Boxplots para observar como os atributos se comportam por classe.

### 2. Pré-processamento
- Separação entre features (`X`) e rótulos (`y`).
- Padronização dos dados com `StandardScaler`.

### 3. Divisão em Conjunto de Treino e Teste
- Separação com `train_test_split` (80% treino, 20% teste, com `stratify=y`).

### 4. Treinamento de Modelos
- **Regressão Logística** (`LogisticRegression`)
- **Árvore de Decisão** (`DecisionTreeClassifier`)

### 5. Avaliação dos Modelos
- Uso da **matriz de confusão** e do `classification_report` com:
  - **Acurácia**: taxa de acertos totais.
  - **Precisão**: taxa de acertos positivos.
  - **Recall**: taxa de cobertura dos positivos reais.
  - **F1-score**: média harmônica entre precisão e recall.

### 6. Tabela Comparativa

| Modelo               | Acurácia | Precisão | Recall | F1-score |
|----------------------|----------|----------|--------|----------|
| Regressão Logística  | 0.97     | 0.97     | 0.97   | 0.97     |
| Árvore de Decisão    | 0.94     | 0.95     | 0.94   | 0.94     |

> Os valores são ilustrativos, baseados nos resultados obtidos. Eles podem variar a cada execução.

### 7. Desafio (Opcional)
- Uso de `GridSearchCV` para encontrar os melhores hiperparâmetros da Árvore de Decisão:
  - `max_depth`
  - `min_samples_split`
- Visualização do heatmap de correlação entre as variáveis.

---

## 🛠️ Tecnologias e Bibliotecas

- Python 3
- pandas
- numpy
- seaborn, matplotlib
- scikit-learn (`sklearn`)

---

## 📌 Como Executar

1. Clone o repositório.
2. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
3. Execute o notebook ou script principal.

---

## 📚 Aprendizados

- Como preparar dados para algoritmos de machine learning.
- Diferença entre algoritmos lineares e baseados em árvore.
- Importância de métricas além da acurácia.
- Uso de validação cruzada para ajuste de hiperparâmetros.

---

