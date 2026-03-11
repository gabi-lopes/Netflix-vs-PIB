# 🎬 Análise de Dados Reais: Netflix e PIB Mundial

Este projeto aplica técnicas de **tratamento de dados (data wrangling)** para reunir, limpar e analisar dois conjuntos de dados — um sobre **filmes e séries da Netflix** e outro sobre o **PIB mundial**, obtido por meio da API do Banco Mundial.  
O objetivo principal é investigar a relação entre o **poder econômico de um país (PIB)** e o **nível de produção audiovisual** presente na plataforma.

---

## 📊 Visão Geral do Projeto

Neste projeto, apliquei as habilidades adquiridas em tratamento de dados para:
- Coletar e extrair dados de diferentes fontes (download manual e API).
- Avaliar e limpar os dados de forma programática.
- Armazenar e combinar diferentes bases.
- Visualizar e interpretar correlações com Python.

---

## 📁 Conjuntos de Dados

### Conjunto 1 — Netflix Titles
- **Tipo:** Arquivo CSV (baixado manualmente do Kaggle)  
- **Descrição:** Contém informações sobre filmes e séries disponíveis na Netflix.  
- **Principais variáveis:**
  - `type`: Filme ou Série  
  - `title`: Título da produção  
  - `director`: Nome do diretor  
  - `cast`: Lista de atores  
  - `country`: País de origem  
  - `release_year`: Ano de lançamento  
  - `rating`: Classificação indicativa  
  - `duration`: Duração (em minutos ou temporadas)  

📈 Este conjunto permite analisar padrões de produção audiovisual por país.

---

### Conjunto 2 — PIB Mundial
- **Tipo:** Dados em JSON obtidos via **API do Banco Mundial**  
- **Método:** Extração automatizada por requisição HTTP.  
- **Principais variáveis:**
  - `country`: Nome do país  
  - `year`: Ano de observação  
  - `gdp (US$)`: PIB total em dólares correntes  

🌍 Este conjunto fornece o contexto econômico necessário para comparação com os dados da Netflix.

---

## 🧠 Pergunta de Pesquisa

> Existe relação entre o PIB de um país e a quantidade de produções da Netflix associadas a ele?

---

## ⚙️ Etapas e Métodos

1. **Coleta de Dados**
   - Dados da Netflix baixados manualmente do Kaggle.  
   - Dados de PIB obtidos via API do Banco Mundial com `requests`.

2. **Avaliação dos Dados**
   - Verificação de completude, consistência e valores ausentes.  
   - Garantia de que cada base possuía mais de 500 observações e pelo menos 2 variáveis.

3. **Limpeza dos Dados**
   - Padronização de nomes de colunas e países.  
   - Remoção de valores nulos e registros irrelevantes.

4. **Junção dos Dados**
   - Combinação das bases por país.  
   - Contagem de títulos da Netflix por país e cruzamento com o PIB.

5. **Análise e Visualização**
   - Cálculo de correlação entre PIB e número de títulos.  
   - Criação de **heatmaps** com a biblioteca **Seaborn**.

---

## 📉 Exemplo de Visualização

A correlação entre PIB e número de produções foi visualizada em um **heatmap**:

![Heatmap](https://img.shields.io/badge/Seaborn-Heatmap-blue?logo=python&style=flat-square)

> O mapa de calor mostra uma **correlação positiva** entre PIB e produção audiovisual.  
> Países com PIB mais elevado tendem a ter mais títulos na Netflix.

---

## 🧩 Tecnologias Utilizadas

| Categoria | Bibliotecas / Ferramentas |
|-----------|---------------------------|
| Manipulação de dados | `pandas`, `numpy` |
| Visualização de dados | `matplotlib`, `seaborn` |
| Coleta de dados | `requests`, `BeautifulSoup` |
| Modelagem / Machine Learning (opcional) | `scikit-learn` |
| Integração com banco de dados | `SQLAlchemy` |
| Processamento de imagens | `Pillow` |

---

## 🧪 Como Executar o Projeto

```bash
# 1. Instale as dependências
pip install numpy pandas matplotlib requests seaborn scikit-learn SQLAlchemy beautifulsoup4 pillow openpyxl

# 2. Execute o notebook
jupyter notebook data_wrangling_project.ipynb
