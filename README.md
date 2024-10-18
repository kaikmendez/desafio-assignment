# Projeto de Processamento de Logs de Servidor Web

Este projeto processa logs de um servidor web, utilizando PySpark no Databricks Community Edition. O código realiza operações de leitura, processamento e análise dos logs para gerar insights como as 10 maiores origens de acesso, endpoints mais acessados, e mais.

## Requisitos:

- Databricks Community Edition ou uma instância Databricks

- PySpark para processamento de dados em grandes volumes

- Bibliotecas externas:
     - py7zr para descompactar arquivos .7z

## Passos para Configuração

### 1. Criar uma Conta no Databricks
- Acesse Databricks Community Edition e crie uma conta gratuita, caso ainda não tenha.

- Crie um Cluster no Databricks para executar seus notebooks.

### 2. Criar e Configurar o Notebook
1. Abra o Databricks Workspace e crie um novo Notebook.

2. Nomeie o notebook como "Processamento de Logs de Servidor Web".

3. No notebook, configure o Cluster criado no passo anterior.

### 3. Instalar a Biblioteca py7zr

Dentro do notebook, instale a biblioteca necessária para descompactação de arquivos executando:

%pip install --upgrade py7zr

### 4. Executar o Código

Copie o código abaixo no notebook e execute célula por célula. 

- Código disponível no arquivo 'desafio-assignment.ipynb'

O código faz o seguinte:

1. Faz download e une dois arquivos .7z de logs compactados.

2. Descompacta o arquivo para o diretório /tmp/descompactado.

3. Carrega e processa os logs, gerando análises como os IPs com mais acessos e erros HTTP.

### 5. Entrega
Após o processamento, você terá os seguintes resultados:

1. As 10 maiores origens de acesso por quantidade de acessos.

2. Os 6 endpoints mais acessados, excluindo arquivos de mídia.

3. A quantidade de Client IPs distintos.

4. O número de dias representados nos dados.

5. Análises sobre o volume total de dados retornado.

6. O dia da semana com o maior número de erros "HTTP Client Error".
