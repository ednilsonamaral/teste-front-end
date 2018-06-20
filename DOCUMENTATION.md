# Documentação do Teste Front-end

Esse documento tem como objetivo esclarecer quais tecnologias foram utilizadas durante o desenvolvimento do teste bem como os motivos para escolhas de tais tecnologias. Além, de, esclarecer a estrutura do projeto que foi utilizado, e, instruções para rodar em seu computador, localmente.


## Tecnologias Utilizadas

- Gulp, como task runner;  
- Stylus, como pré-processador CSS;
- Jeet, como sistema de grid;  
- Rupture, lib responsável para trabalhar com breakpoints juntamente com Stylus;  
- Pug, como template engine HTML.


## Metodologias

Uma das metodologias utilizadas no CSS é a combinação RSCSS + ITCSS.

O RSCSS é simplesmente um conjunto de ideias para orientar o seu processo de construção de CSS sustentável para qualquer site ou aplicação, escolhido aqui, nesse projeto, para facilitar a criação de novos elementos e componentes.

O ITCSS é responsável pela nossa arquitetura CSS, deixando-a e permitindo-a que seja escalável e de fácil manutenção. No ITCSS, a estrutura é definida conforme as seguintes especificações:

**SETTINGS ==>** configurações básicas, variáveis globais (cores), espaçamentos  
**TOOLS ==>** mixins e funções necessárias  
**GENERIC ==>** resets, box-sizing, etc  
**BASE ==>** estilos para headings, blockquotes, a, buttons, etc. estilizações BÁSICAS  
**OBJECTS ==>** pequenos pedaços da interface. padrões de botões, listas, paineis, etc  
**COMPONENTS ==>** componentes/elementos criados  
**TRUMPS ==>** também conhecido como helpers  


## Estrutura do Projeto

```
| _source >> para exclusivamente para DESENVOLVIMENTO
---| assets
------| css >> toda a estrutura CSS, com o ITCSS
---------| base
---------| componentes
---------| elements
---------| generic
---------| objects
---------| settings
---------| tools
---------| trumps
---------| main.css
---------| main.styl
------| img >> todas as imagens antes de serem otimizadas
------| js >> todos os arquivos JS antes de serem concatenados e minimificados
---| _includes >> partes dos layouts
---| index.pug

| _public >> para exclusivamente para PRODUÇÃO, após compilado a partir da _source
---| assets
------| css
---------| styles.min.css
------| img >> todas as imagens otimizadas
------| js >> todos os arquivos JS concatenados e minimificados
---| _includes >> partes dos layouts
---| index.html

| tasks >> todas as tarefas do GULP, separadas

| gulpfile.js >> arquivo principal do GULP, chamando as tarefas
| config.json >> arquivo responsável por dizer quais diretórios estão os arquivos, para serem chamados no Gulp
| DOCUMENTATION.md
```


## Instalação Local

Ao clonar o repositório, antes de executar qualquer comando, tenha instalado globalmente:

- Node.js;  
- Gulp;
- Plugin EditorConfig em seu editor de códigos.

Tendo tudo instalado, basta executar o comando `npm install` para instalar todas as dependências necessárias do projeto, e, em seguida, execute o comando `npm run dev`. Então, ele vai executar o Gulp e abrir no navegador a página do projeto.
