# 📊 Projeto: Geração Distribuída de Energia no Brasil  
### CMPINAM — Modelagem, Análise e Avaliação

---

## 👥 Integrantes do Grupo
- **Nycholas Victor Hayashida de Oliveira**  
- **Eduarda Machado Carreira**  
- **Antonio Rafael Debroi Magalhães**

---

## 🌱 Tema do Projeto
Este projeto tem como objetivo analisar dados reais de **Geração Distribuída de Energia no Brasil**, com foco em usinas fotovoltaicas conectadas à rede, e desenvolver **modelos de Aprendizado de Máquina** capazes de prever a **potência instalada (kW)** com base em características cadastrais das unidades geradoras.

O estudo inclui:
- Análise exploratória dos dados (EDA)  
- Limpeza, pré-processamento e engenharia de atributos  
- Construção e comparação de modelos preditivos  
- Interpretação dos resultados obtidos  
- Identificação dos fatores que mais influenciam a potência instalada  

---

## 🗂️ Estrutura do Repositório

```
├── Parte2_Completa_Com_Texto_e_Codigo.ipynb   # Notebook com texto + códigos de ML  
├── Parte2_Modelagem_Avaliacao.ipynb           # Notebook apenas com os códigos  
├── json de Geração Distribuída de Energia no Brasil.json  # Base de dados utilizada
├── README.md                                   # Documento de apresentação
```

---

## ⚙️ Instruções de Execução

### **1. Dependências necessárias**
Antes de rodar os notebooks, instale as bibliotecas necessárias:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

### **2. Como executar**
1. Baixe o notebook `.ipynb` deste repositório.  
2. Abra no **Jupyter Notebook**, **Google Colab** ou qualquer ambiente compatível.  
3. Certifique-se de que o arquivo JSON esteja no mesmo diretório ou ajuste o caminho no notebook.  
4. Execute as células sequencialmente.  

---

## 🔍 Principais Etapas do Projeto

### **1. Análise Exploratória (EDA)**
- Distribuição da potência instalada  
- Mapa de calor das correlações  
- Gráficos por estado, classe de fornecimento e modalidade de consumo  
- Identificação de padrões regionais e operacionais  

### **2. Pré-processamento**
- Remoção de colunas irrelevantes  
- Conversão da potência para tipo numérico  
- One-Hot Encoding de variáveis categóricas  
- Normalização com StandardScaler  
- Divisão Treino/Teste (80/20)  

### **3. Modelos de Machine Learning aplicados**
- **Regressão Linear (baseline)**  
- **K-Nearest Neighbors (KNN)**  
- **Random Forest Regressor** *(melhor desempenho)*  

### **4. Métricas de Avaliação**
- R² (Coeficiente de Determinação)  
- RMSE (Erro Quadrático Médio)  
- MAE (Erro Absoluto Médio)  

---

## 🏆 Principais Resultados

| Modelo               | R²   | RMSE (kW) | MAE (kW) |
|---------------------|------|-----------|----------|
| Regressão Linear    | 0.41 | 6.2       | 3.1      |
| KNN                 | 0.78 | 3.0       | 1.7      |
| **Random Forest**   | **0.93** | **1.9** | **0.8**  |

### ✔ Modelo vencedor: **Random Forest Regressor**

Motivos:
- Captura relações não lineares  
- Robusto a outliers  
- Excelente capacidade preditiva (R² > 0.90)  
- Permite interpretar importância das variáveis  

### 🔑 Variáveis mais importantes:
1. Município  
2. Classe de fornecimento  
3. Modalidade de consumo  
4. Estado (UF)  
5. Tipo da unidade consumidora  

---

## 📌 Conclusões Gerais

- A potência instalada pode ser prevista com **alta precisão** utilizando modelos não lineares.  
- A Geração Distribuída no Brasil apresenta **forte dependência regional**.  
- Fatores socioeconômicos e operacionais explicam variações significativas.  
- O Random Forest mostrou-se a abordagem mais eficiente e robusta.  
- Com mais atributos (clima, renda, irradiação solar), o modelo pode atingir desempenho ainda melhor.  

---

## 📬 Contato
Para dúvidas ou melhorias, entre em contato com os integrantes do grupo.

---
