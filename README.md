# Meus Proventos - Dashboard de Rendimentos

Dashboard web responsivo para visualização e análise de proventos financeiros (dividendos, JCP e rendimentos), criado a partir de planilha Excel.

## Funcionalidades

- **Importação de dados**: carregue a planilha `.xlsx` via upload ou drag-and-drop
- **Filtros interativos**: por código do ativo, ano, mês, tipo de evento e instituição
- **KPIs**: valor total recebido, ativo destaque, instituição destaque, média mensal
- **Top 5 ativos**: ranking dos ativos que mais pagaram
- **Top 3 corretoras**: ranking das instituições que mais receberam
- **Por tipo de evento**: ativo que mais pagou em cada categoria (Dividendo, JCP, Rendimento)
- **Por ano**: ativo que mais pagou em cada ano
- **Gráfico de rosca**: distribuição por tipo de evento e por instituição com valores e percentuais
- **Gráfico de linha**: progressão de rendimentos ao longo do tempo (anual ou mensal por ano)
- **Tabela completa**: todos os registros com paginação (15/página), ordenação por coluna e conversão de datas

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

1. Abra o arquivo `Meus Proventos.html` em qualquer navegador moderno (Chrome, Edge, Firefox)
2. Clique em **Importar Dados** ou arraste o arquivo `projetoProventoDio.xlsx` para a área indicada
3. Utilize os filtros para refinar a visualização
4. Alterne entre tema **claro** e **escuro** com o botão no cabeçalho

> Se o carregamento automático não funcionar ao abrir pelo protocolo `file://`, basta importar manualmente o arquivo Excel.

## Estrutura do projeto

```
📁 DIO_Aceleração_AI_Reports_Excel/
├── Meus Proventos.html    # Dashboard completo (arquivo único)
├── projetoProventoDio.xlsx # Planilha de dados (fonte)
└── README.md              # Este arquivo
```

## Como foi criado

O dashboard foi desenvolvido como arquivo HTML único para simplificar o uso — sem dependências de build ou servidor. Toda a lógica de processamento dos dados, renderização dos gráficos e interação com o usuário está contida em um único arquivo.

As bibliotecas Chart.js e SheetJS são carregadas via CDN, e a fonte Inter via Google Fonts.

## Requisitos

- Navegador com suporte a ES6+ e Canvas API
- Conexão com internet (primeiro carregamento para CDNs)

## Licença

Projeto de estudo — DIO Aceleração AI.
