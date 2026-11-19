# 📊 Statistics Rocketseat Challenge

Mini projeto de introdução ao curso de **Machine Learning**, desenvolvido a partir de um desafio da [Rocketseat](https://www.rocketseat.com.br/). O objetivo é praticar os primeiros passos de análise de dados e estatística descritiva com **Pandas**, explorando um conjunto simples de faturamento mensal.

---

## 📌 Sumário

- [Sobre o desafio](#-sobre-o-desafio)
- [Tecnologias](#-tecnologias)
- [Conjunto de dados](#-conjunto-de-dados)
- [O que foi feito](#-o-que-foi-feito)
- [Resultados](#-resultados)
- [Como executar](#-como-executar)
- [Aprendizados](#-aprendizados)
- [Próximos passos](#-próximos-passos)

---

## 🎯 Sobre o desafio

A proposta é transformar um dicionário Python com dados de faturamento em um `DataFrame` do Pandas e, a partir dele:

1. Calcular uma medida estatística (média do faturamento);
2. Visualizar os dados em gráficos para facilitar a interpretação.

---

## 🛠 Tecnologias

| Ferramenta | Uso |
| --- | --- |
| [Python 3](https://www.python.org/) | Linguagem principal |
| [Pandas](https://pandas.pydata.org/) | Manipulação dos dados e cálculo estatístico |
| [Matplotlib](https://matplotlib.org/) | Backend de geração dos gráficos |
| [Jupyter Notebook](https://jupyter.org/) | Ambiente de execução e exploração |

---

## 🗂 Conjunto de dados

Os dados são definidos diretamente no notebook, em um dicionário com duas colunas:

| Coluna | Descrição |
| --- | --- |
| `data_ref` | Data de referência do faturamento (mês) |
| `valor` | Valor faturado no período (R$) |

<details>
<summary>Ver os 12 registros</summary>

| data_ref | valor |
| --- | ---: |
| 2023-01-01 | 400.000 |
| 2020-02-01 | 890.000 |
| 2021-03-01 | 760.000 |
| 2022-04-01 | 430.000 |
| 2023-05-01 | 920.000 |
| 2023-06-01 | 340.000 |
| 2020-07-01 | 800.000 |
| 2021-08-01 | 500.000 |
| 2022-09-01 | 200.000 |
| 2023-10-01 | 900.000 |
| 2022-11-01 | 570.000 |
| 2023-12-01 | 995.000 |

</details>

---

## 🔍 O que foi feito

**1. Criação do DataFrame**

```python
df = pd.DataFrame.from_dict(dict_faturamento)
```

**2. Média do faturamento**

```python
df.valor.mean()
```

**3. Gráfico de barras** — faturamento por data de referência

```python
df.plot.bar(x='data_ref', y='valor', title='Faturamento por mês',
            xlabel='Data de referência', ylabel='Valor do faturamento', color='blue')
```

**4. Gráfico de linha** — evolução do faturamento

```python
df.plot.line(x='data_ref', y='valor', title='Faturamento por mês',
             xlabel='Data de referência', ylabel='Valor do faturamento', color='green')
```

---

## 📈 Resultados

| Métrica | Valor |
| --- | ---: |
| Quantidade de registros | 12 |
| **Média do faturamento** | **R$ 642.083,33** |
| Menor faturamento | R$ 200.000 (2022-09) |
| Maior faturamento | R$ 995.000 (2023-12) |

Os gráficos de barras e de linha estão no notebook e mostram a variação do faturamento entre os registros.

---

## ▶️ Como executar

```bash
# 1. Clone o repositório
git clone https://github.com/mateh3007/statistics-rocketseat-challenge.git
cd statistics-rocketseat-challenge

# 2. (Opcional) Crie e ative um ambiente virtual
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate

# 3. Instale as dependências
pip install pandas matplotlib notebook

# 4. Abra o notebook
jupyter notebook
```

Depois, abra o arquivo `statistcs.ipynb` e execute as células em ordem.

---

## 💡 Aprendizados

- Converter estruturas Python (`dict`) em `DataFrame` com `pd.DataFrame.from_dict`;
- Acessar colunas e aplicar funções estatísticas (`mean`);
- Gerar gráficos rapidamente com a API `.plot` do Pandas;
- Escolher o tipo de gráfico conforme o objetivo: barras para comparar valores e linha para observar tendências.

---

<p align="center">Feito durante o curso de Machine Learning · Desafio Rocketseat</p>
