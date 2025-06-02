# chemical-solubility-prediction
🧪 Análise Comparativa de Modelos de Regressão para Previsão de Solubilidade

Este repositório contém o código e o artigo referentes à análise comparativa de diferentes modelos de regressão aplicados à previsão da solubilidade de compostos químicos. O projeto foi desenvolvido como parte das atividades acadêmicas do curso de Ciência da Computação (UFC).

## 📄 Artigo

> **Título**: Uma Análise Comparativa de Modelos para Solubilidade de Substâncias Químicas  
> **Autores**: Victor Santos, Guilherme Sales de Andrade, Samuel Nicolau Alves Ribeiro da Silva  
> **Instituição**: Universidade Federal do Ceará - Departamento de Teleinformática  
>  
> O artigo apresenta uma comparação entre os seguintes modelos:
- Regressão Linear (OLS)
- Regressão Ridge
- Regressão Lasso
- PCR (Regressão por Componentes Principais)
- PLS (Mínimos Quadrados Parciais)
- Rede Neural para regressão

[📑 Clique aqui para acessar o artigo completo (PDF)](./HW02___2024_2.pdf)

---

## 📊 Dataset

O conjunto de dados contém **1267 compostos químicos**, descritos por:
- 208 **fingerprints binários**
- 16 **descritores quantitativos**
- 4 **descritores contínuos**

A variável alvo é a **solubilidade** dos compostos.

---

## ⚙️ Métodos e Implementações

O notebook `homework2_teste.ipynb` contém todas as etapas descritas no artigo:

### 🔍 1. Análise Exploratória e Pré-processamento
- Padronização dos dados
- Cálculo de assimetria, correlação e seleção de variáveis

### 📈 2. Modelos de Regressão
- **OLS** com `statsmodels` e implementação manual
- **Ridge** e **Lasso** com tuning de hiperparâmetros (λ)
- **PCR** e **PLS** com variação do número de componentes

### 🤖 3. Rede Neural
- Arquitetura com 2 camadas ocultas (258 e 128 neurônios)
- Função de ativação: ReLU
- Otimizador: Adam
- Função de perda: MSE

### 📉 4. Validação
- Validação cruzada (k-fold, k=5)
- Métricas utilizadas: **R²** e **RMSE**

---

## 📈 Resultados

| Modelo         | R²      | RMSE    |
|----------------|---------|---------|
| OLS            | 0.788   | 0.941   |
| Ridge          | 0.876   | 0.730   |
| Lasso          | -       | -       |
| PCR            | 0.849   | 0.804   |
| PLS            | 0.876   | 0.729   |
| Rede Neural    | 0.889   | 0.689   |

> 🔍 A rede neural apresentou o melhor desempenho, embora modelos lineares como Ridge e PLS também tenham se mostrado eficientes e interpretáveis.

---

## 📁 Arquivos

- `HW02___2024_2.pdf`: artigo acadêmico completo em PDF  
- `homework2_teste.ipynb`: notebook com todas as análises, modelos e gráficos
- `Datasets`: Todos os datasets usados.

---

## 📚 Referências

- Kuhn, M., & Johnson, K. (2013). *Applied Predictive Modeling*. Springer.  
- [Medium: Regularização Lasso e Ridge](https://medium.com/@jackelinegleme/regulariza%C3%A7%C3%A3o-lasso-l1-e-ridge-l2-a12efacc5fb3)  
- [Notebook Colab 1](https://colab.research.google.com/drive/1ezN6F16JNDS_CfGjXfxeLBzDSIgduMzW?usp=sharing)  
- [Notebook Colab 2](https://colab.research.google.com/drive/18L4uwSSqIh_P_POzark-I5GvBquyDm69?usp=sharing)

---

## 👨‍💻 Como executar

Para rodar o projeto localmente:

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
