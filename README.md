# Pipeline de Dados - Sistema de Eventos e Festas

Projeto da disciplina de Extração e Análise de Dados. O objetivo era montar um pipeline
completo de dados a partir de três fontes diferentes e responder perguntas de negócio
com base nelas.

## Fontes de dados

- **SQL** — histórico de compras de ingressos (usuário, festa, quantidade)
- **JSON** — catálogo de festas, simulando dados vindos de uma API (nome, categoria, preço)
- **HTML** — página com os preços atualizados de cada festa no site

## O que o pipeline faz

1. **Extração** das três fontes acima.
2. **Limpeza** — trata valores ausentes, corrige tipos de dado e padroniza texto.
3. **Integração** das três fontes usando um identificador numérico único (`id_festa`),
   evitando problemas de nomes de festa escritos de formas diferentes em cada fonte.
4. **Transformação** — criação de novas colunas, como valor gasto por compra, diferença
   de preço entre a API e o site, e faixa de preço.
5. **Análise exploratória** — estatísticas descritivas, agrupamentos e detecção de outliers.
6. **Visualização** — gráficos comparando gasto por usuário, preços entre fontes e
   ingressos vendidos por festa.
7. **Insights finais** — respostas às perguntas: quem mais gastou, festa mais vendida,
   média de gasto e diferença de preço entre as fontes.

## Tecnologias

Python, Pandas, SQLite, BeautifulSoup (para ler o HTML) e Matplotlib.

## Como rodar

Abra o notebook `Projeto_Eventos_Festas_Corrigido.ipynb` no Jupyter ou Google Colab e
execute as células em ordem. Os arquivos de origem (`eventos.sql`, `festas.json.json`,
`index.html`) precisam estar na mesma pasta do notebook.
