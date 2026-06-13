# BI de Gestão de Demandas — Unimed Serra Gaúcha

Projeto acadêmico da disciplina Projeto em Business Intelligence e Analytics — PUCRS.

## Sobre o Projeto

Solução de Business Intelligence para gestão e priorização de demandas organizacionais
na Unimed Serra Gaúcha, utilizando Matriz de Urgência e Impacto com dashboard no Power BI
e análise preditiva em Python (Google Colab).

## Estrutura do Repositório

- `notebook/` — Notebook Python com análise exploratória e modelo preditivo
- `dados/` — Dicionário de dados
- `dashboards/` — Capturas de tela do dashboard Power BI

## Ferramentas Utilizadas

- Microsoft Excel Online (SharePoint) — coleta e armazenamento de dados
- Power BI Desktop — dashboards e visualizações
- Google Colab (Python) — análise preditiva com scikit-learn
- GitHub — documentação e versionamento

## Como Executar o Notebook

1. Acesse https://colab.research.google.com/
2. Faça upload do arquivo `.ipynb`
3. Faça upload do CSV `demandas_historico.csv` no seu Google Drive
4. Execute célula por célula na ordem

## Dicionário de Dados

| Campo | Tipo | Descrição |
|-------|------|-----------|
| Nome da Demanda | Texto | Título da demanda |
| Área/Canal | Categoria | Área responsável |
| Tipo | Categoria | Tipo da demanda |
| Responsável | Texto | Nome do responsável |
| Prazo Desejado | Data | Data limite esperada |
| Urgência (1-10) | Número | Nota de urgência |
| Impacto (1-10) | Número | Nota de impacto |
| Quadrante | Calculado | Crítica / Urgente / Estratégica / Backlog |
| Status | Categoria | Nova / Em andamento / Aguardando / Backlog / Concluída |
| Criado em | Data | Data de cadastro |
| Prazo_em_Dias | Calculado | Diferença entre prazo e criação |
| Em_Atraso | Binário | 1 = em risco de atraso, 0 = dentro do prazo |

## Modelo Preditivo

- **Algoritmo:** Regressão Linear (scikit-learn)
- **Variável alvo:** Prazo em dias
- **Variáveis preditoras:** Urgência, Impacto, Área/Canal, Tipo
- **Metodologia:** KDD (Seleção → Pré-processamento → Transformação → Modelagem → Avaliação)

## Autora

Sarah Marques de Oliveira  
