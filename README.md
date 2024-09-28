# Previsor de Preços de Voos

MVP - Engenharia de Software - PUC Rio  
Aimone Seawright

## Descrição do Projeto

Este projeto prevê o preço de passagens aéreas com base em diversos fatores (tais como data do voo, numero de paradas, compania aera...). O **backend** utiliza um modelo de machine learning treinado, enquanto o **frontend** oferece uma interface amigável para que os usuários possam inserir dados e obter previsões.

Ele está dividido em dois repositórios: **frontend** (React) e **backend** (Flask API), que são organizados da seguinte forma:

root/ 
├── [backend/](https://github.com/adseawright/flight-price-backend) 
└── [frontend/](https://github.com/adseawright/flight-price-frontend)

## Apresentação do Projeto

Aqui está a apresentação completa do projeto, explicando seu funcionamento e principais funcionalidades:

[![Apresentação do Projeto](https://img.youtube.com/vi/nTh0aGA7bfM/maxresdefault.jpg)](https://youtu.be/nTh0aGA7bfM)

> Clique no vídeo para assistir no YouTube.

### Notebook do Modelo de Machine Learning

O notebook utilizado para treinar o modelo de machine learning pode ser acessado aqui:  
[Notebook do Colab](https://colab.research.google.com/drive/1nlHEk9jymDp1WJpjVaQhMIlYYzvuXbwL?authuser=1#scrollTo=9GTCfU3niy9n)

#### Detalhes do Notebook:
- **Dataset**: Flight Price Prediction Dataset Freshly Cleaned, de Chidinma Okonta e Shubham Bathwal.
- **Informações do Dataset**: O dataset contém 300.257 registros e 24 características, fornecendo dados sobre opções de reserva de voos no site "Easemytrip" para viagens aéreas entre as 6 principais cidades da Índia. Os preços estão em Rúpias Indianas.
- **Objetivo**: O notebook gera um modelo de machine learning para prever o preço de uma passagem aérea com base em fatores como companhia aérea, cidades de origem e destino, duração do voo, e outros.

## Como Configurar o Projeto

![Flight Price Predictor](https://github.com/adseawright/flight-price-main/raw/main/flight-price-predictor.JPG)

### Pré-requisitos:

- **Node.js** e **npm** (para o frontend)
- **Python 3.8+** e **pip** (para o backend)

### Estrutura de Diretórios

1. Clone os dois repositórios na seguinte estrutura:

   ```bash
   git clone https://github.com/adseawright/flight-price-frontend.git frontend
   git clone https://github.com/adseawright/flight-price-backend.git backend

Após clonar, você terá a seguinte estrutura de arquivos:

Root/ 
├── frontend/ # Repositório do frontend 
└── backend/ # Repositório do backend   

### Descompactando o Arquivo do Modelo

ATENÇÃO: O arquivo do modelo está no formato `.zip` no diretório `\backend\api\MachineLearning\models\modelo_final.zip`.

Você vai precisar descompactar este arquivo dentro do mesmo diretório para o backend conseguir acessá-lo. 

Execute o seguinte comando no terminal para descompactar (Ambiente Windows):

   tar -xf backend\api\MachineLearning\models\modelo_final.zip -C backend\api\MachineLearning\models\


### Configurando o Backend (ambiente Windows)

1. **Navegue até o diretório `backend`**:
   ```bash
   cd backend

2. **Crie um ambiente virtual (opcional, mas recomendado)**:

   ```bash
   python -m venv venv
   venv\Scripts\activate

3. **Instale as dependências**:
   ```bash
   pip install -r requirements.txt

4. **Inicialize o banco de dados**:
   ```bash
   python scripts\init_db.py

5. **Execute o backend**:
   ```bash
   python api\app.py

### Configurando o Frontend

1. **Navegue até o diretório `frontend`**:
   ```bash
   cd ..\frontend

2. **Instale as dependências**:
   ```bash
   npm install

3. **Execute o frontend**:
   ```bash
   npm start

## Executando Testes no Backend

1. Para rodar os testes no backend e verificar o funcionamento do modelo de machine learning:
   ```bash
   pytest backend/tests/test_model.py



