
# SmartSales - Analise Exploratória de Dados e KPIs

O objetivo deste projeto é realizar uma análise exploratória de dados de vendas, produtos, clientes e vendedores, utilizando Python e Jupyter Notebook. O projeto permite execução em dois modos: offline, através de um dataset CSV incluso no repositório, e online, conectado ao Google Sheets via autenticação híbrida.

## Como funciona

1. O notebook verifica e instala dependências automaticamente.  
2. Os dados podem ser carregados de duas formas:  
   - Offline: leitura do arquivo `data/samples/SmartSales_Dados.csv`.  
   - Online: leitura da planilha no Google Sheets, via Colab (autenticação automática) ou Service Account local.  
3. Colunas são padronizadas para nomes canônicos, facilitando a consistência da análise.  
4. São realizadas validações básicas de integridade (quantidade, preço, datas).  
5. São calculados KPIs principais como receita, lucro, quantidade de pedidos e itens vendidos.  
6. Resultados são exibidos em tabelas e gráficos no notebook.

## Funcionalidades

- Execução híbrida (Colab ou local com Jupyter).  
- Modo offline com dataset exemplo incluso no repositório.  
- Padronização automática de colunas para análise consistente.  
- Validações de dados: quantidades, preços, datas.  
- Cálculo de KPIs de vendas, clientes, produtos e vendedores.  
- Geração de gráficos simples para visualização dos resultados.  

## Organização do Projeto

```
smartsales-eda/
├── notebooks/
│   └── SmartSales_Analise.ipynb   # Notebook principal do projeto
├── data/
│   └── samples/
│       └── SmartSales_Dados.csv   # Dataset de exemplo para execução offline
├── requirements.txt               # Dependências do projeto
├── README.md                      # Instruções de uso
├── .gitignore                     # Arquivos ignorados pelo Git
```

## Execução

### Modo offline (rápido para testar)
1. Abra `notebooks/SmartSales_Analise.ipynb` no Colab ou VS Code.  
2. Execute a primeira célula.  
3. O notebook irá carregar `data/samples/SmartSales_Dados.csv` e gerar dimensões sintéticas (Produtos, Clientes, Vendedores) para calcular os KPIs.

### Modo Google Sheets
1. Colab: apenas abra o notebook, a autenticação acontece de forma automática com sua conta Google.  
2. Local (VS Code/Jupyter):  
   - Crie uma Service Account no Google Cloud.  
   - Compartilhe a planilha com o e-mail da Service Account.  
   - Baixe o arquivo `.json` da credencial.  
   - Defina a variável de ambiente `GDRIVE_SA_JSON` apontando para o caminho do `.json`.  

Exemplo no PowerShell:
```powershell
$env:GDRIVE_SA_JSON="C:\Users\Matheus\OneDrive\Credenciais\sa.json"
```

Exemplo no Linux/macOS:
```bash
export GDRIVE_SA_JSON="/home/usuario/credenciais/sa.json"
```

## Requisitos

- Python 3.10 ou superior  
- Bibliotecas: pandas, matplotlib, gspread, google-auth, google-auth-oauthlib  

## Considerações finais

O projeto foi desenvolvido como parte de um módulo da especialização em Ciência de Dados e Inteligência Artificial. Ele serve como base para análises exploratórias, podendo ser expandido para novos relatórios, integrações com dashboards ou análises preditivas.

Autor: Matheus Rossi Carvalho  
LinkedIn: https://www.linkedin.com/in/matheusrossicarvalho/