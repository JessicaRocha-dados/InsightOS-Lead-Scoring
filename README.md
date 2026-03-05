# InsightOS - Lead Scoring Inteligente para Martech

O **InsightOS** é uma solução de inteligência de dados desenvolvida para otimizar a conversão de leads e reduzir o desperdício de verba em campanhas de tráfego pago (Google Ads, Meta Ads e LinkedIn Ads).

Utilizando algoritmos de Machine Learning, o projeto identifica leads com maior probabilidade de conversão, permitindo que o time comercial foque nos contatos certos e as plataformas de anúncios sejam otimizadas apenas para usuários de alto valor.

## O Problema de Negócio
Muitas empresas de Martech enfrentam o desafio do "lead curioso": usuários que preenchem formulários mas não têm intenção de compra. Isso gera:
1.  Sobrecarga do time comercial.
2.  Poluição dos algoritmos de leilão com conversões de baixa qualidade.
3.  Custo por Aquisição (CPA) elevado.

## 🛠️ Tecnologias Utilizadas
* **Linguagem:** Python [cite: 2025-11-18-2026-02-19]
* **Modelagem:** XGBoost Classifier
* **Processamento de Dados:** Pandas, NumPy [cite: 2025-11-18-2026-02-19]
* **Avaliação:** Scikit-learn (Precision, Recall, F1-Score)
* **Exportação:** Joblib

## 📊 Metodologia e Resultados
Durante o desenvolvimento, testamos diferentes abordagens para garantir o equilíbrio entre encontrar compradores e evitar alarmes falsos:

* **Ajuste de Pesos (scale_pos_weight=1.38):** Compensamos o desbalanceamento dos dados para dar mais importância à classe de compradores.
* **Threshold Tuning:** Otimizamos o limiar de decisão (40%) para maximizar a captura de leads qualificados (Recall de 74%).

**Performance Final do Modelo Exportado:**
* **Acurácia Geral:** 78.20%
* **Precisão (Compradores):** 0.73
* **Recall (Compradores):** 0.72

## 🏗️ Estrutura do Repositório
* `01_exploracao_e_limpeza.ipynb`: Tratamento inicial e limpeza dos dados. [cite: 2026-01-16]
* `02_analise_exploratoria.ipynb`: Insights visuais sobre o comportamento dos leads. [cite: 2026-01-16]
* `03_modelo_machine_learning.ipynb`: Treinamento, otimização e validação do XGBoost.
* `/modelos`: Contém o arquivo `insightos_xgb_v1.pkl` pronto para implementação server-side.

## 🚀 Próximos Passos (Checklist)
- [ ] Fase 5: Desenho da arquitetura de ativação via GTM Server-Side.
- [ ] Fase 6: Dashboard Executivo no Power BI (CPA Otimizado vs. CPA Real).

---
**Desenvolvido por Jéssica Rocha** | [LinkedIn](https://www.linkedin.com/in/jessicarocha-dados)