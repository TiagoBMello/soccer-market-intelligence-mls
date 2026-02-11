# ⚽ Football Market Intelligence  
## MLS 2025 – Análise Estratégica de Mercado de Jogadores

---

## 📌 1. Visão Geral do Projeto

Este projeto simula a atuação de um departamento profissional de análise de mercado no futebol.
Utilizando dados brutos da temporada 2025 da Major League Soccer (MLS), o objetivo é identificar jogadores com alto desempenho estatístico que possam representar oportunidades estratégicas de contratação para a temporada seguinte.
O projeto integra engenharia de dados, modelagem relacional, análise estatística e visualização executiva, reproduzindo um cenário real de tomada de decisão orientada por dados.

---

## 🎯 2. Problema de Negócio

Clubes com orçamento limitado precisam maximizar retorno esportivo e financeiro nas janelas de transferência.
Pergunta central do projeto:
> Quais jogadores da MLS 2025 apresentaram desempenho superior e podem representar oportunidades subvalorizadas no mercado para 2026?

---

## 🏗️ 3. Arquitetura de Dados

O projeto segue uma estrutura completa de pipeline analítico:
RAW DATA (Tabelas HTML - FBref)  
↓  
Extração em Python  
↓  
Transformação e Limpeza (pandas / numpy)  
↓  
Banco de Dados Relacional (PostgreSQL)  
↓  
Feature Engineering  
↓  
Dataset Final (Camada Gold)  
↓  
Power BI + Excel  
Essa abordagem demonstra organização, rastreabilidade e separação clara entre camadas de dados.

---

## 🛠️ 4. Tecnologias Utilizadas

### 🐍 Python
- `pandas` → Manipulação e transformação de dados
- `numpy` → Cálculos estatísticos
- `matplotlib` → Visualizações exploratórias
- `requests` / `read_html` → Extração de dados web

### 🗄️ Banco de Dados
- PostgreSQL  
  Modelagem relacional com normalização, chaves primárias e estrangeiras.

### 📊 Business Intelligence
- Power BI → Dashboard interativo
- Excel → Simulador executivo e análises dinâmicas

---

## 🗄️ 5. Modelagem do Banco de Dados

### Tabelas Principais

**players**
- player_id
- nome
- idade
- nacionalidade
- posição

**teams**
- team_id
- nome_clube

**seasons**
- season_id
- ano

**player_season_stats**
- player_id
- team_id
- season_id
- minutos
- gols
- assistências
- finalizações
- passes
- métricas defensivas
- indicadores por 90 minutos

A modelagem relacional permite flexibilidade analítica e escalabilidade futura.

---

## 📊 6. Metodologia Analítica

### 📈 Padronização por 90 minutos
Permite comparação justa entre jogadores com diferentes tempos de jogo.

Exemplos:
- gols_por90
- assistencias_por90
- participacao_gol_por90

---

### 📐 Player Efficiency Score (PES)

Índice proprietário composto por múltiplas métricas ponderadas, como:

- Contribuição ofensiva
- Eficiência de finalização
- Participação na construção de jogadas
- Ajuste por posição

O PES permite criar um ranking objetivo de performance.

---

### 🔎 Identificação de Jogadores Subvalorizados

Critérios utilizados:
- Jogadores no quartil superior de performance
- Abaixo da mediana em proxies de mercado (idade, minutos, contexto de equipe)
- Alta eficiência relativa

Métodos estatísticos aplicados:
- Z-Score
- Ranking por posição
- Análise de dispersão

---

## 📦 7. Entregáveis do Projeto

- Pipeline ETL documentado
- Banco de dados relacional estruturado
- Métricas proprietárias de eficiência
- Dashboard interativo em Power BI
- Simulador executivo em Excel
- Documentação técnica completa
- README estratégico para apresentação

---

## 🚀 8. Diferencial Estratégico

Este projeto demonstra:

- Engenharia de dados aplicada
- Modelagem relacional
- Análise estatística orientada a negócio
- Construção de métricas proprietárias
- Visualização executiva para tomada de decisão
- Organização de projeto em padrão profissional

Simula um cenário real de atuação como Analista de Dados no mercado esportivo ou corporativo.

---

## 📌 9. Resultado Esperado

Geração de uma shortlist estratégica de jogadores da MLS 2025 com alto potencial de custo-benefício para contratação na temporada 2026.
