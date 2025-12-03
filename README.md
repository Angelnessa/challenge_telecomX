# 📈 Análise de Evasão de Clientes (Churn) - TelecomX

## 🎯 Visão Geral do Projeto

Este projeto consiste na Análise Exploratória de Dados (EDA) de um conjunto de dados de clientes da **TelecomX** com o objetivo principal de **identificar os principais fatores preditores de Churn** (evasão de clientes).

O resultado da análise visa subsidiar a empresa com insights acionáveis e recomendações estratégicas para a redução da taxa de evasão, que atualmente é de aproximadamente **26.5%** na base de dados analisada.

## 📁 Estrutura do Repositório

* **`Challenge_Telecom_X.ipynb`**: Notebook Jupyter contendo todo o pipeline de análise, desde o carregamento dos dados até a engenharia de recursos e a Análise Exploratória de Dados (EDA).
* **`README.md`**: Este arquivo com a descrição e os resultados do projeto.

## 🛠️ Tecnologias Utilizadas

O projeto foi desenvolvido em ambiente Jupyter, utilizando a linguagem Python e as seguintes bibliotecas principais:

* `Python`
* `Pandas`: Para manipulação e limpeza de dados.
* `requests`: Para o carregamento dos dados via URL.
* `Matplotlib` / `Seaborn` (Implícito na EDA): Para a criação de visualizações e gráficos.

## 🔍 Metodologia e Pipeline de Análise

O processo de análise seguiu um pipeline robusto de Data Science, conforme detalhado no notebook:

1.  **Carregamento de Dados:** Os dados foram importados a partir de um arquivo JSON hospedado externamente.
2.  **Limpeza e Estruturação:**
    * Colunas aninhadas (JSON) foram transformadas em um DataFrame tabular.
    * Valores ausentes em `Charges_Total` (Cobranças Totais) foram identificados e preenchidos com `0`, visto que correspondiam a clientes com `tenure` (tempo de contrato) nulo.
3.  **Engenharia de Recursos (Feature Engineering):**
    * Criação de indicadores binários, como `HasInternet` e `HasPhone`.
    * Cálculo da métrica de consumo diário (`Contas_Diarias`) para melhor entendimento do perfil de gastos.
4.  **Análise Exploratória (EDA):** Visualizações de dados para identificar a correlação entre as variáveis e a variável alvo (`Churn`).

## ✨ Principais Resultados e Insights

A EDA revelou fatores de Churn que exigem atenção imediata:

| Fator de Risco | Taxa de Churn (%) | Insight Chave |
| :--- | :--- | :--- |
| **Contrato Mensal** | ~42% | O tipo de contrato é o maior preditor de evasão. |
| **Tenure (Baixo)** | Alto no 1º ano | Clientes nos primeiros 12 meses são os mais vulneráveis. |
| **Serviço Fibra Ótica** | Alta | Problemas de qualidade ou preço não competitivo podem estar ligados a este serviço. |
| **Ausência de Suporte** | Alta | A falta de serviços de valor agregado, como Suporte Técnico e Proteção de Dispositivo, aumenta o risco. |
| **Senior Citizen** | ~40% | Este grupo demográfico é menos fiel e requer atenção especial. |

## 🚀 Recomendações Estratégicas

Com base nos insights, as seguintes ações são recomendadas para a TelecomX:

1.  **Incentivo à Fidelização:** Lançar campanhas agressivas para converter clientes de contrato **Mensal** em contratos de **1 ou 2 anos**.
2.  **Monitoramento Proativo:** Criar um programa de engajamento focado nos **primeiros seis meses** de contrato, principalmente para clientes de alto risco (ex: Fibra Ótica).
3.  **Reforço de Valor Agregado:** Incluir serviços de **Suporte Técnico** de forma gratuita ou subsidiada nos pacotes básicos para aumentar as "âncoras" de retenção.
4.  **Atenção ao Público Sênior:** Desenvolver ofertas e canais de atendimento simplificados e dedicados ao segmento de clientes **Senior Citizen**.

## 🤝 Como Visualizar o Projeto

Para executar o notebook e replicar a análise:
1.  Abra o arquivo `Challenge_Telecom_X.ipynb` em um ambiente Jupyter (JupyterLab, Google Colab ou VS Code).
2.  Execute as células sequencialmente para visualizar o pré-processamento, a EDA e as visualizações geradas.

---
*Desenvolvido como parte de um desafio de Análise de Dados.*
