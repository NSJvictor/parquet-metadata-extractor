# Extrator de Metadados Parquet

Esta aplicação permite extrair metadados de arquivos Parquet e gerar um arquivo Excel com informações detalhadas sobre os campos e tipos de dados.

## Requisitos

- Python 3.8 ou superior
- Node.js 14 ou superior
- npm ou yarn

## Estrutura do Projeto

```
parquet-metadata-extractor/
├── backend/
│   ├── app.py
│   ├── extract_parquet_metadata.py
│   └── requirements.txt
└── frontend/
    ├── public/
    │   ├── index.html
    ├── src/
    │   ├── App.js
    │   ├── App.css
    │   ├── index.js
    │   └── index.css
    └── package.json
```

## Instalação e Execução

### Backend (Flask)

1. Clone o repositório:
   ```bash
   git clone <url-do-repositorio>
   cd parquet-metadata-extractor
   ```

2. Crie e ative um ambiente virtual:
   ```bash
   # Criar o ambiente virtual
   cd backend
   python -m venv venv

   # Ativar no Windows
   venv\Scripts\activate

   # Ativar no Linux/Mac
   source venv/bin/activate
   ```

3. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

4. Execute o servidor Flask:
   ```bash
   python app.py
   ```
   O servidor backend estará rodando em http://localhost:5000

### Frontend (React)

1. Abra um novo terminal (mantenha o backend rodando)

2. Navegue até a pasta do frontend:
   ```bash
   cd parquet-metadata-extractor/frontend
   ```

3. Instale as dependências:
   ```bash
   npm install
   ```

4. Inicie o servidor de desenvolvimento:
   ```bash
   npm start
   ```
   A aplicação frontend estará disponível em http://localhost:3000

## Como Usar

1. Acesse a aplicação web no navegador em http://localhost:3000

2. Clique no botão "Selecionar Arquivos Parquet" para escolher os arquivos .parquet que deseja analisar

3. Após selecionar os arquivos, clique em "Gerar Excel"

4. Quando o processamento for concluído, clique no botão "Baixar Arquivo Excel"

5. O arquivo Excel gerado conterá as seguintes informações:
   - Nome do arquivo Parquet
   - Nome de cada campo/coluna
   - Tipo de dado da coluna (com detecção avançada)
   - Observações (estatísticas, valores nulos, identificação de tipos especiais)
   - Uma coluna de descrição vazia para ser preenchida manualmente
