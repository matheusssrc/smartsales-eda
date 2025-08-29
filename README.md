
# SmartSales – Análise Exploratória (EDA) e KPIs

Este repositório está **pronto para subir** no GitHub.  
Ele roda de dois jeitos:
- **Colab:** autenticação pela sua conta Google e leitura da planilha.
- **Local (VS Code/Jupyter):** Service Account via `GDRIVE_SA_JSON` **ou** **modo offline** com `data/samples/SmartSales_Dados.csv`.

## Como executar (rápido)

### A) Modo offline (recomendado para testar agora)
1. Abra `notebooks/SmartSales_Analise.ipynb` no VS Code (Jupyter) ou Colab.
2. Execute a **primeira célula**.  
   Ela instala dependências se necessário e carrega o arquivo `data/samples/SmartSales_Dados.csv`.
3. O notebook gera **dimensões sintéticas** (Produtos, Clientes, Vendedores) a partir dos IDs do CSV para permitir o cálculo de KPIs (preço/custo são gerados de forma determinística).

### B) Modo Google Sheets
1. **Colab:** só abrir o notebook e rodar; a autenticação aparece automaticamente.
2. **VS Code local:** crie uma Service Account, compartilhe a planilha com o e-mail da SA e defina a variável:
   - PowerShell:
     ```powershell
     $env:GDRIVE_SA_JSON="C:\Users\Matheus\OneDrive\Credenciais\sa.json"
     ```
   - Linux/macOS:
     ```bash
     export GDRIVE_SA_JSON="/home/usuario/credenciais/sa.json"
     ```

## Estrutura
```
smartsales-eda/
├─ notebooks/
│  └─ SmartSales_Analise.ipynb
├─ data/
│  └─ samples/
│     └─ SmartSales_Dados.csv
├─ requirements.txt
├─ README.md
├─ .gitignore
```

## Notas
- **Dimensões sintéticas** são apenas para rodar offline. Em produção, substitua pela leitura real das abas Produtos, Clientes e Vendedores do Google Sheets.
- **Não comite credenciais**. `.gitignore` já inclui padrões sensíveis.
