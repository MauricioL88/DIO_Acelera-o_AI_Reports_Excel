# Meus Proventos - Dashboard de Rendimentos

Dashboard web responsivo para visualização e análise de proventos financeiros (dividendos, JCP e rendimentos) a partir de planilha Excel. Publicado via GitHub Pages.

## Funcionalidades

- **Importação de dados**: carregue a planilha `.xlsx` via upload ou drag-and-drop
- **Dados mock embutidos**: dados de exemplo são carregados automaticamente quando nenhuma planilha está disponível
- **Normalização de instituições**: nomes duplicados de corretoras são unificados automaticamente (ex.: XP, NU, Toro)
- **Filtros interativos**: por código do ativo, ano, mês, tipo de evento e instituição
- **KPIs**: valor total recebido, ativo destaque, instituição destaque, média mensal
- **Top 5 ativos**: ranking dos ativos que mais pagaram
- **Top 3 corretoras**: ranking das instituições que mais receberam
- **Por tipo de evento**: ativo que mais pagou em cada categoria (Dividendo, JCP, Rendimento)
- **Por ano**: ativo que mais pagou em cada ano
- **Gráfico de rosca**: distribuição por tipo de evento e por instituição com valores e percentuais
- **Gráfico de linha**: progressão de rendimentos ao longo do tempo (anual; mensal quando um ano é selecionado)
- **Tabela completa**: todos os registros com paginação (15/página), ordenação por coluna e conversão de datas seriais do Excel
- **Tema claro/escuro**: alternância persistida via `localStorage`
- **Redesenho automático**: gráficos são recriados ao alternar o tema via `MutationObserver`
- **Restaurar dados**: botão para limpar dados carregados e recarregar os dados mock

## Tecnologias

| Tecnologia | Versão | Finalidade |
|---|---|---|
| HTML5 | — | Estrutura da aplicação |
| CSS3 | — | Estilização, temas, responsividade |
| JavaScript | ES6+ | Lógica da aplicação |
| [Chart.js](https://www.chartjs.org/) | 4.4.7 | Gráficos (rosca e linha) |
| [SheetJS](https://sheetjs.com/) (xlsx) | 0.18.5 | Leitura de arquivos Excel no navegador |
| [Google Fonts](https://fonts.google.com/) | Inter | Tipografia moderna |

## Como usar

1. Acesse [https://mauriciol88.github.io/DIO_Acelera-o_AI_Reports_Excel/](https://mauriciol88.github.io/DIO_Acelera-o_AI_Reports_Excel/) ou abra o `index.html` em qualquer navegador moderno (Chrome, Edge, Firefox)
2. Os dados de exemplo carregam automaticamente; clique em **Importar Dados** ou arraste o arquivo `projetoProventoDio.xlsx` para a área indicada para carregar seus dados
3. Utilize os filtros para refinar a visualização
4. Alterne entre tema **claro** e **escuro** com o botão no cabeçalho
5. Para voltar aos dados de exemplo, clique no botão **↺** (restaurar)

> Se o carregamento automático não funcionar ao abrir pelo protocolo `file://`, basta importar manualmente o arquivo Excel.

## Estrutura do projeto

```
📁 DIO_Aceleração_AI_Reports_Excel/
├── index.html             # Dashboard completo (arquivo único, raiz)
├── docs/
│   └── index.html         # Cópia para GitHub Pages (fonte /docs)
├── projetoProventoDio.xlsx # Planilha de dados (fonte, ignorada pelo git)
├── .gitignore             # Ignora arquivos .xlsx
└── README.md              # Este arquivo
```

## Deploy

O projeto é publicado automaticamente via **GitHub Pages** a partir da branch `main`, usando o diretório `/docs` como fonte. O mesmo `index.html` está presente na raiz e em `/docs/` para compatibilidade com ambas as configurações de Pages.

Repositório: `git@github.com:MauricioL88/DIO_Acelera-o_AI_Reports_Excel.git`

## Detalhes técnicos

- **Dados mock**: um array `MOCK_DATA` com ~150 registros é embutido no HTML para demonstração imediata
- **Normalização**: o mapa `NORMALIZE_INST` unifica variações de nomes de instituições (ex.: `"XP INVESTIMENTOS CCTVM S/A."` → `"XP INVESTIMENTOS CCTVM S/A"`)
- **Conversão de datas**: a função `excelSerialToDate()` converte números seriais do Excel (época 25569) para data legível
- **Persistência**: o tema escolhido é salvo em `localStorage` e restaurado ao recarregar
- **Redesenho**: um `MutationObserver` monitora o atributo `data-theme` e reconstrói os gráficos quando o tema muda

## Requisitos

- Navegador com suporte a ES6+ e Canvas API
- Conexão com internet (primeiro carregamento para CDNs)

## Licença

Projeto de estudo — DIO Aceleração AI.
