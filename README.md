# 🌱 Estudo da Produção de Soja no Paraná: Análise e Previsão com dados do LSPA/IBGE

Este projeto de **Business Intelligence (BI)** e **Analytics** analisa e prevê a produção de soja no estado do Paraná, utilizando dados históricos do **LSPA/IBGE** no período de **2020 a 2024**.  
O objetivo foi identificar qual modelo preditivo — **Random Forest, ARIMA ou Holt-Winters** — apresenta o melhor desempenho na previsão da produção.

O Paraná é o **segundo maior produtor de soja do Brasil**, tornando esta análise estratégica para o planejamento agrícola, econômico e logístico.

## Métricas Estratégicas (KPIs)

- **Área Plantada (ha):** total de hectares destinados ao cultivo de soja.  
- **Área Colhida (ha):** hectares efetivamente colhidos ao final de cada ciclo produtivo.  
- **Produção (t):** volume total de soja produzido no estado, em toneladas.  
- **Rendimento Médio (kg/ha):** produtividade média calculada pela razão entre produção e área colhida.  
- **Crescimento Percentual Anual da Produção (%):** variação relativa ano a ano.  
- **Previsão da Produção:** projeções realizadas a partir de 2025 com o modelo de melhor desempenho.  

---

## Arquitetura da Solução

A solução de BI e Analytics foi construída com as seguintes camadas:

- **Fonte de Dados:** LSPA/IBGE (arquivos CSV).  
- **Processamento e Análise:** Python (Google Colab/Jupyter) → Pandas, NumPy, Statsmodels, Scikit-learn.  
- **Visualização e BI:** Power BI.  
- **Repositório de Código:** GitHub.  

### 🔹 Diagrama da Arquitetura
<img width="618" height="878" alt="image" src="https://github.com/user-attachments/assets/38e88fab-f39c-4431-975d-918066ed3fcd" />

---

##  Análise Preditiva e Comparação de Modelos

Três modelos foram implementados e comparados:  

| Modelo         | MAE        | RMSE       | R²     | MAPE (%) |
|----------------|-----------:|-----------:|-------:|---------:|
| Random Forest  | 251,201.27 | 459,984.87 | 0.97   | 1.25     |
| ARIMA          | 1,036,003.78 | 1,063,119.12 | -18.41 | 5.55 |
| Holt-Winters   | 4,006,709.04 | 4,013,141.00 | -275.53 | 21.52 |

### Conclusão:
O modelo **Random Forest** apresentou o melhor desempenho, com R² = 0.97 e MAPE de apenas 1.25%.  

---

## Visualizações no Power BI

### Aba Histórico (2020–2024)
- Evolução da produção anual.  
- Comparação entre área plantada e colhida.  
- Crescimento percentual da produção.  
- Rendimento médio.  

<img width="591" height="330" alt="image" src="https://github.com/user-attachments/assets/9b5458bc-0da7-49f6-a0a1-2244206acd0b" />

---

### Aba Previsões (2025+)
- Produção prevista para 2025–2027.  
- Comparação com a safra de 2024.  
- Distribuição mensal das previsões.  

<img width="591" height="332" alt="image" src="https://github.com/user-attachments/assets/978aba71-6b88-470d-ad96-9a57b766fb3b" />


---

##  Previsões Futuras (2025–2027)

As previsões geradas com o modelo **Random Forest** foram exportadas em formato CSV.  
Exemplo de saída:

| Ano | Mês | Produção Prevista (toneladas) |
|-----|-----|-------------------------------|
| 2025 | 1 | 18.585.427,42|
| ... | ... | ... |
| 2027 | 12 | 18.642.785,58 |

---

##  Estrutura do Repositório


| Arquivo                             | Descrição                                                                 |
|-------------------------------------|---------------------------------------------------------------------------|
| area_colhida_soja_PR_2020-2024.csv  | Dados originais de área colhida (LSPA/IBGE)                               |
| area_plantada_soja_PR_2020-2024.csv | Dados originais de área plantada (LSPA/IBGE)                              |
| producao_soja_PR_2020-2024.csv      | Dados originais de produção (LSPA/IBGE)                                   |
| rendimento_soja_PR_2020-2024.csv    | Dados originais de rendimento médio (LSPA/IBGE)                           |
| df_soja_tratado.csv                 | Dados tratados e padronizados (para BI/Analytics)                         |
| previsoes_soja_mensais.csv          | Produções previstas pelo modelo vencedor (2025+)                          |
| fase2.ipynb                         | Notebook em Python com análises, modelos e comparações                    |
| fase2.pbix                          | Dashboard em Power BI (histórico + previsões)                             |
| projeto_bi_e_analytics-fase01.pdf   | Relatório da Fase 1 do projeto                                            |
| README.md                           | Documentação principal do repositório                                     |


**Todo o código, dados e dashboards estão disponíveis neste repositório GitHub:**  [Acesse o repositório aqui](https://github.com/SabrinaDantas/soja_previsao_pucrs)


## Autor

**Sabrina Dantas**  
Disciplina: Projeto em Business Intelligence e Analytics – PUCRS Online 
