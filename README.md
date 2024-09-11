# 🏆 Multithreading Web Scraping com IMDb
![GitHub repo size](https://img.shields.io/github/repo-size/BrunoOliveira16/ecommerce-react?style=for-the-badge)
![Languages](https://img.shields.io/github/languages/count/BrunoOliveira16/ecommerce-react?style=for-the-badge)
![Status projeto](https://img.shields.io/badge/STATUS-CONCLUIDO-GREEN?style=for-the-badge)

## ✔️ Tecnologias Utilizadas
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-4B0082?style=for-the-badge&logo=beautifulsoup&logoColor=white)
![Requests](https://img.shields.io/badge/Requests-000000?style=for-the-badge&logo=requests&logoColor=white)




## 📌 Resumo do Projeto
Este projeto realiza **web scraping** no site **IMDb** para extrair informações sobre os filmes mais populares. Ele utiliza a biblioteca `requests` para fazer requisições HTTP e a `BeautifulSoup` para parsear o HTML. Além disso, o código faz uso de **multithreading** para otimizar a coleta de dados, tornando o processo mais rápido ao lidar com múltiplos filmes simultaneamente.

## Funcionalidades

- Coleta informações dos filmes mais populares no IMDb, incluindo:
  - **Título** do filme.
  - **Ano de lançamento**.
  - **Nota** dos filmes.
  - **Sinopse**.
- Armazena os dados extraídos em um arquivo CSV.
- Utiliza até 20 threads para processar múltiplos links de filmes simultaneamente, acelerando a coleta de dados.

## Tecnologias Utilizadas

- **Python** para a execução do script.
- **Requests** para realizar as requisições HTTP ao IMDb.
- **BeautifulSoup** para fazer o parsing do HTML e extrair as informações relevantes.
- **CSV** para armazenar os dados dos filmes.
- **Multithreading** com a biblioteca `concurrent.futures` para processar múltiplos filmes em paralelo.

## Instalação

1. Clone este repositório:

    ```bash
    git clone https://github.com/EmersonPenelli/Multithreading-py
    ```

2. Instale as dependências necessárias:

    ```bash
    pip install requests beautifulsoup4
    ```

3. Execute o script:

    ```bash
    python multithreading.py
    ```

## Estrutura do Código

- **Cabeçalhos globais**: Utilizados para evitar bloqueios de requisições por parte do IMDb, simulando um navegador.
- **Função `extract_movie_details`**: Extrai detalhes de cada filme como título, data de lançamento, nota e sinopse.
- **Função `extract_movies`**: Coleta os links de cada filme da lista de mais populares no IMDb e gerencia o processamento usando múltiplas threads.
- **Função `main`**: Ponto de entrada do código. Faz a requisição à página principal dos filmes mais populares e inicia o processo de extração.

## Exemplo de Saída

Os dados coletados são armazenados em um arquivo `movies.csv` com o seguinte formato:

```csv
Título, Ano de Lançamento, Nota, Sinopse
"Filme 1", "2023", "8.6", "Sinopse do filme 1"
"Filme 2", "2022", "7.9", "Sinopse do filme 2"
