# Projeto de Machine Learning: Previsão de Preços de Pizza

Este é um projeto simples de machine learning que prevê o preço de uma pizza com base em seu diâmetro. O projeto utiliza um modelo de regressão linear treinado com um conjunto de dados de pizzas e seus respectivos preços, e a gestão de dependências é feita com **Poetry**.

## 📝 Descrição do Projeto

O objetivo principal deste projeto é demonstrar um fluxo de trabalho básico de machine learning, incluindo:
* Análise e visualização de dados.
* Treinamento de um modelo de regressão.
* Criação de uma aplicação web interativa para realizar previsões.

## 🗂️ Arquivos no Repositório

* `pizzas.csv`: O conjunto de dados contendo o diâmetro e o preço das pizzas.
* `testes.ipynb`: Um Jupyter Notebook para a exploração de dados, visualização e treinamento do modelo de machine learning.
* `app.py`: O script da aplicação web criada com Streamlit que permite ao usuário interagir com o modelo.

## 🍕 Dataset: `pizzas.csv`

O conjunto de dados é um arquivo CSV simples com duas colunas:
* `diametro`: O diâmetro da pizza em centímetros.
* `preco`: O preço da pizza em Reais (R$).

Os dados apresentam uma forte correlação linear, como pode ser visto no gráfico de dispersão abaixo, onde o aumento do diâmetro corresponde a um aumento no preço.

![Gráfico de Dispersão de Preço por Diâmetro](https://raw.githubusercontent.com/alanz0ka/projeto-ml/main/scatterplot.png)

*(Nota: O gráfico acima foi gerado no notebook `testes.ipynb`)*.

## 🤖 Modelo de Machine Learning: `testes.ipynb`

O notebook `testes.ipynb` detalha o processo de criação do modelo:
1.  **Carregamento dos Dados:** Os dados de `pizzas.csv` são carregados em um DataFrame do pandas.
2.  **Visualização:** Um gráfico de dispersão é criado para visualizar a relação entre o diâmetro e o preço.
3.  **Treinamento do Modelo:** Um modelo de `LinearRegression` da biblioteca `scikit-learn` é instanciado e treinado (`fit`) com os dados, usando o `diametro` como a variável independente (X) e o `preco` como a variável dependente (Y).

## 🖥️ Aplicação Web: `app.py`

A aplicação web, desenvolvida com a biblioteca Streamlit, oferece uma interface de usuário simples para prever o preço de uma pizza.

* **Entrada do Usuário:** A aplicação solicita que o usuário insira o diâmetro da pizza desejada.
* **Previsão:** Utilizando o modelo de regressão linear treinado, a aplicação calcula o preço previsto para o diâmetro informado.
* **Resultado:** O valor previsto da pizza é exibido para o usuário.

### Como Executar a Aplicação com Poetry

Este projeto utiliza [Poetry](https://python-poetry.org/) para gerenciamento de dependências.

1.  **Instale o Poetry:**
    Se você ainda não o tem, siga as [instruções de instalação oficiais](https://python-poetry.org/docs/#installation).

2.  **Instale as dependências:**
    Após clonar o repositório, navegue até a pasta raiz e execute o comando abaixo. Ele lerá o arquivo `pyproject.toml` e instalará as dependências em um ambiente virtual.
    ```bash
    poetry install
    ```

3.  **Execute o aplicativo Streamlit:**
    Use `poetry run` para executar o script dentro do ambiente virtual gerenciado pelo Poetry.
    ```bash
    poetry run streamlit run app.py
    ```

4.  Abra o navegador no endereço local fornecido pelo Streamlit para interagir com a aplicação.

## 🛠️ Tecnologias Utilizadas

* **Python:** Linguagem de programação principal.
* **Poetry:** Para gerenciamento de dependências.
* **Pandas:** Para manipulação e análise de dados.
* **Scikit-learn:** Para criar e treinar o modelo de regressão linear.
* **Streamlit:** Para criar a aplicação web interativa.
* **Jupyter Notebook:** Para exploração de dados e prototipagem do modelo.