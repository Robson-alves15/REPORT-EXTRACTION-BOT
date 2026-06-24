#  Report Extraction Bot

Bot de automação para extração e organização de relatórios de **Cashback por parceiro**, desenvolvido com **Selenium** e **Python**. O bot acessa o sistema interno via navegador, baixa os relatórios de cada parceiro automaticamente e os organiza em pastas por percentual de cashback (50% ou 100%).

---

## O que o bot faz

```
Lê planilha de parceiros
        │
        ▼
Faz login no sistema interno
        │
        ▼
Para cada parceiro:
  ├── Filtra por nome e mês
  ├── Extrai relatório (.xlsx)
  ├── Renomeia o arquivo
  └── Move para pasta 50% ou 100%
        │
        ▼
Compila todos os relatórios
em um arquivo final por pasta
```

---

##  Organização dos arquivos gerados

```
Downloads/
├── Relatórios Cashback 50%/
│   ├── Relatório-cashback-ParcerioA.xlsx
│   ├── Relatório-cashback-ParcerioB.xlsx
│   └── Compilado_Relatórios Cashback 50%.xlsx
│
└── Relatórios Cashback 100%/
    ├── Relatório-cashback-ParcerioC.xlsx
    └── Compilado_Relatórios Cashback 100%.xlsx
```

---

##  Tecnologias

| Tecnologia | Uso |
|------------|-----|
| **Python** | Linguagem principal |
| **Selenium** | Automação do navegador Chrome |
| **Pandas** | Leitura da planilha e compilação dos relatórios |
| **dotenv** | Gerenciamento seguro de credenciais |
| **logging** | Rastreamento de erros e execução |
