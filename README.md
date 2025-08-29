# SmartSales - Analise Exploratória de Dados e KPIs

O objetivo deste projeto é realizar uma análise exploratória de dados de vendas, produtos, clientes e vendedores, utilizando Python e Jupyter Notebook. O projeto pode ser executado em dois modos: offline, através de um dataset CSV incluso no repositório, ou online, conectado ao Google Sheets via autenticação híbrida.

## Como funciona

1. O notebook verifica e instala dependências automaticamente.  
2. Os dados podem ser carregados de duas formas:  
   - Offline: leitura do arquivo `data/samples/SmartSales_Dados.csv`.  
   - Online: leitura da planilha no Google Sheets, via Colab (autenticação automática) ou Service Account local.  
3. As colunas são padronizadas para nomes canônicos, garantindo consistência nas análises.  
4. O sistema realiza validações básicas de integridade (quantidade, preço, datas).  
5. São calculados KPIs principais como receita, lucro, número de pedidos e itens vendidos.  
6. Os resultados são exibidos em tabelas e gráficos diretamente no notebook.

## Funcionalidades

- Execução híbrida (Google Colab ou local via Jupyter).  
- Dataset de exemplo incluso no repositório para execução offline.  
- Padronização automática de colunas.  
- Validação de integridade dos dados.  
- Cálculo de KPIs de vendas, produtos, clientes e vendedores.  
- Visualização dos resultados em tabelas e gráficos.  

## Organização do Projeto

Este repositório está dividido em:

- `notebooks/`: contém o notebook principal do projeto.  
- `data/`: armazena datasets de exemplo para execução offline.  
- Arquivos de configuração: `.gitignore`, `requirements.txt` e `README.md`.

## Estrutura de Pastas

```
.
├── notebooks/
│   └── SmartSales_Analise.ipynb         # Notebook principal
│
├── data/
│   └── samples/
│       └── SmartSales_Dados.csv         # Dataset de exemplo para execução offline
│
├── requirements.txt                     # Dependências do projeto
├── README.md                            # Instruções e documentação
└── .gitignore                           # Arquivos ignorados pelo Git
```

## Requisitos

- Python 3.10 ou superior  
- Bibliotecas: pandas, matplotlib, gspread, google-auth, google-auth-oauthlib  

## Considerações

- Este projeto pode ser expandido para novas métricas, relatórios interativos e integração com ferramentas de BI.  
- O dataset incluso é apenas um exemplo, sendo possível conectar planilhas reais via Google Sheets.  
- O notebook já instala dependências automaticamente para facilitar a execução em qualquer ambiente.

## Licença

MIT License

---

**Autor:** Matheus Rossi Carvalho  
**Contato:** [LinkedIn](https://www.linkedin.com/in/matheus-rossi-carvalho/)
