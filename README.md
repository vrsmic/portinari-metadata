# **Exploração Visual das Correspondências de Cândido Portinari através de Metadados Textuais**
#### *Micaele Brandão e Mateus Bandeira*

## Sobre o Projeto

Este projeto realiza uma análise exploratória das correspondências históricas do pintor brasileiro Cândido Portinari através de metadados textuais. Utilizando técnicas de web scraping e ciência de dados, transformamos documentos históricos em insights visuais para facilitar a compreensão da trajetória pessoal e profissional do artista.

## Objetivos

- Coletar metadados de aproximadamente 5.800 correspondências disponíveis no acervo digital do Projeto Portinari
- Estruturar e limpar dados históricos extraídos via web scraping
- Realizar análises exploratórias visuais sobre remetentes, destinatários, períodos e tipos de correspondência
- Preservar e facilitar o acesso a informações culturais relevantes

## Tecnologias Utilizadas

- **Python 3.9+**
- **Pandas** - manipulação e análise de dados
- **Altair** - visualizações interativas
- **Selenium & Playwright** - web scraping automatizado
- **Jupyter Notebook** - desenvolvimento e documentação

## Estrutura do Projeto

```
├── AV2.ipynb                    # Notebook principal com análises
├── scrapper.ipynb               # Web scraping básico (Selenium)
├── scrapper_1.1.ipynb          # Web scraping otimizado
├── scrapper_rapido.ipynb       # Web scraping paralelo (Playwright)
├── Data/
│   ├── dados_finais.csv        # Dataset consolidado e tratado
│   └── dados_*.csv             # Datasets intermediários
└── Images/
    └── Paleta.png              # Paleta de cores do projeto
```

## Pipeline de Dados

1. **Coleta**: Web scraping do site DocVirt com ~9.126 páginas
2. **Consolidação**: Junção de múltiplas extrações e remoção de duplicatas
3. **Extração de Metadados**: Parsing de campos estruturados (remetente, destinatário, data, tipo, etc.)
4. **Limpeza**: Padronização de formatos e tratamento de valores ausentes
5. **Análise Visual**: Geração de gráficos exploratórios com Altair

## Campos Extraídos

- `id_doc`: Identificador único (CO_XXXX)
- `remetente`: Autor da correspondência
- `destinatario`: Destinatário da correspondência
- `data`: Data de envio (formato DD/MM/AAAA)
- `tipo_doc`: Tipo (Carta, Telegrama, etc.)
- `onomastico`: Menções a terceiros
- `memo_resumo`: Resumo do conteúdo

## Como Executar

```bash
# Clone o repositório
git clone [https://github.com/vrsmic/portinari-metadata.git]

# Instale as dependências
pip install pandas altair selenium playwright webdriver-manager

# Execute o notebook principal
jupyter notebook AV2.ipynb
```

> **Nota**: O web scraping já foi realizado. Os dados finais estão em `Data/dados_finais.csv`.

## Resultados

O dataset final contém **4.147 correspondências com texto válido**, cobrindo aproximadamente 70% do acervo digitalizado. As análises visuais revelam padrões de comunicação do artista ao longo de sua carreira.

## Paleta de Cores

O projeto utiliza uma paleta personalizada inspirada nas obras de Portinari:
- Azul: `#4F6F8C`
- Dourado: `#BF8821`
- Vermelho: `#A62014`
- Vinho: `#59150E`

## Fonte dos Dados

[Projeto Portinari - DocVirt](https://www.docvirt.com/docreader.net/DocReader.aspx?bib=coportinari)

## Licença

Este projeto é desenvolvido para fins acadêmicos.

---

*Desenvolvido como trabalho final da disciplina de Introdução à Ciência de Dados*
