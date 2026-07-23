# 📊 Análise Exploratória de Dados do ENEM 2019

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)](https://plotly.com/)

---

## 📋 Sobre o Projeto

Este projeto consiste em uma **Análise Exploratória de Dados (EDA)** completa dos microdados do **ENEM 2019**, disponibilizados pelo INEP. O objetivo é compreender o perfil dos participantes, identificar padrões de desempenho e explorar correlações entre características demográficas, socioeconômicas e as notas obtidas nas provas.

O ENEM (Exame Nacional do Ensino Médio) é a principal porta de entrada para o ensino superior no Brasil, sendo utilizado no SISU, ProUni, FIES e em mais de 50 instituições portuguesas. Compreender os dados dos candidatos pode gerar insights valiosos para políticas educacionais e estratégias de ensino.

O projeto foi desenvolvido em **Google Colab** com **Python** e processa uma base com **5.095.171 registros**, explorando variáveis demográficas, socioeconômicas e de desempenho.

---

## 🎯 Objetivos

### Principais
- **Caracterizar o perfil** dos participantes do ENEM 2019 (sexo, raça, renda, escolaridade dos pais, etc.).
- **Identificar correlações** entre variáveis demográficas/socioeconômicas e as notas nas provas.
- **Explorar padrões** de desempenho por região, tipo de escola, renda e outros fatores.

### Secundários
- **Comparar** a viabilidade de trabalhar com a base completa versus uma amostra de 10%.
- **Gerar visualizações interativas** para facilitar a interpretação dos dados.
- **Documentar** todo o processo de limpeza, transformação e análise.

---

## 📊 Dataset

### Fonte
Os dados utilizados são os **Microdados do ENEM 2019**, disponibilizados publicamente pelo INEP ([link para download](https://www.gov.br/inep/pt-br/acesso-a-informacao/dados-abertos/microdados/enem)).

### Características
| Característica | Descrição |
|----------------|-----------|
| **Total de registros** | 5.095.171 candidatos |
| **Total de colunas** | 76 colunas (após limpeza, reduzido para 56) |
| **Período** | 2019 |
| **Formato original** | CSV (encoding `latin-1`, separador `;`) |
| **Formato processado** | Parquet (otimizado para análise) |

### Variáveis principais
- **Demográficas:** sexo, idade, raça/cor, estado civil, nacionalidade.
- **Educacionais:** tipo de escola, conclusão do ensino médio, escolaridade dos pais.
- **Socioeconômicas:** renda familiar.
- **Desempenho:** notas em Ciências da Natureza, Ciências Humanas, Linguagens, Matemática e Redação.
- **Presença:** indicadores de comparecimento por área.

---

## 🔍 Principais Perguntas Respondidas

1. **Qual o perfil típico do participante do ENEM 2019?**
2. **Como as notas se distribuem por área do conhecimento?**
3. **Existe correlação entre renda familiar e desempenho?**
4. **A escolaridade dos pais influencia as notas dos candidatos?**
5. **Quais são as diferenças de desempenho por raça/cor e sexo?**
6. **Como os candidatos se distribuem geograficamente?**
7. **É viável trabalhar com uma amostra de 10% da base?**
8. **Quais variáveis têm maior correlação com o desempenho?**

---

## 📈 Principais Insights

### Perfil do Candidato "Padrão"
- **Sexo:** Feminino (59,5%)
- **Idade:** 18 anos (faixa etária 4)
- **Raça/Cor:** Parda (46,4%)
- **Renda familiar:** Até R$ 1.497,00
- **Escolaridade dos pais:** Sem ensino superior completo (88% dos pais, 82% das mães)
- **Estado civil:** Solteiro(a)

### Distribuição das Notas
- **Matemática:** Maior média (523,1) e maior dispersão (desvio padrão 109,1)
- **Redação:** Distribuição bimodal, com picos em 500 e 700 pontos
- **Ciências Humanas e Linguagens:** Médias próximas (507 e 520)

### Correlações Identificadas
| Fator | Correlação com Notas |
|-------|----------------------|
| **Renda familiar** | Moderada (0,3–0,5, mais forte em Matemática) |
| **Escolaridade dos pais** | Moderada a forte (diferença de ~50 pontos na mediana) |
| **Raça/Cor** | Candidatos brancos e amarelos têm médias superiores |
| **Sexo** | Homens melhores em Exatas; mulheres em Redação e Linguagens |

### Comparação Base Completa vs. Amostra de 10%
- **Representatividade:** A amostra manteve todas as distribuições e correlações.
- **Performance:** Redução de ~80% no tempo de processamento.
- **Conclusão:** A amostra é viável para análises exploratórias rápidas.

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Descrição |
|------------|-----------|
| **Python** | Linguagem principal |
| **Pandas** | Manipulação e análise de dados |
| **NumPy** | Operações matemáticas |
| **Matplotlib** | Visualizações estáticas |
| **Seaborn** | Visualizações estatísticas |
| **Plotly** | Visualizações interativas |
| **PyArrow** | Conversão para formato Parquet |
| **Google Colab** | Ambiente de desenvolvimento |

---

## 📁 Estrutura do Repositório

```
enem-eda-2019/
│
├── notebooks/
│   ├── Projeto_Enem_Base_Completa.ipynb   # Análise com 5M+ registros
│   └── Projeto_Enem_Amostra10.ipynb   # Análise com amostra de 10%
│
├── data/
│   └── (os dados não estão incluídos no repositório devido ao tamanho)
├── README.md                              # Este arquivo
```

---

## 🚀 Como Executar o Projeto

### Pré‑requisitos
- Python 3.8+
- Google Colab (recomendado) ou Jupyter Notebook
- Acesso aos microdados do ENEM 2019 (download manual ou via script)

### Passo a Passo

1. **Clone o repositório**
```bash
git clone [https://github.com/Henrique08-dev/Projeto_EDA_Enem.git]
cd enem-eda-2019
```

2. **Instale as dependências**
```bash
pip install -r requirements.txt
```

3. **Baixe os dados**  
   Faça o download dos microdados do ENEM 2019 no site do INEP e coloque o arquivo `MICRODADOS_ENEM_2019.csv` na pasta `data/`.

4. **Execute o notebook**  
   Abra o notebook no Google Colab ou Jupyter e execute as células sequencialmente.

5. **Ajuste os caminhos**  
   Se necessário, ajuste o caminho do arquivo CSV no notebook:
   ```python
   caminho_csv = '/caminho/para/MICRODADOS_ENEM_2019.csv'
   ```

### Alternativa – Amostra de 10%
Para análises mais rápidas, o notebook da amostra utiliza `sample(frac=0.1)` para reduzir o dataset.

---

## 📚 Conclusão

A análise exploratória revelou padrões importantes sobre o perfil dos participantes do ENEM 2019 e suas relações com o desempenho acadêmico. Os principais achados incluem:

- **Desigualdade educacional:** Renda e escolaridade dos pais estão fortemente correlacionadas com o desempenho, especialmente em Matemática.
- **Perfil predominante:** O candidato típico é mulher, parda, com 18 anos e renda familiar baixa.
- **Disparidades regionais:** A distribuição geográfica mostra concentração no Sudeste e Nordeste.
- **Viabilidade da amostragem:** A amostra de 10% mostrou-se representativa e eficiente para análises exploratórias.

Esses insights podem subsidiar políticas públicas, orientar estratégias pedagógicas e ajudar instituições a personalizar campanhas de preparação para o exame.

---

## 🔮 Próximos Passos

- Aplicar modelos de **Machine Learning** para prever notas com base em variáveis demográficas.
- Analisar a influência do **tipo de escola** (pública/privada) no desempenho.
- Explorar a relação entre **treineiros** e resultados.
- Desenvolver um **dashboard interativo** (Power BI/Streamlit) para visualização dinâmica.
- Expandir a análise para outros anos (2018, 2020, etc.) para identificar tendências temporais.

---

## 📬 Contato

**Henrique Albuquerque Araújo**  
📧 he.fla3@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/henrique-araujo-analista-de-dados/)  
🐙 [GitHub](https://github.com/Henrique08-dev)
