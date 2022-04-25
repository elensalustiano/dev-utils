# Empacotadores de módulos (Module bundlers)

Podemos executar JavaScript dentro do arquivo HTML utilizando a tag <i>script</i>. Porém, conforme o projeto vai crescendo, queremos manter a organização separando o código em vários módulos e importando no nosso HTML, além de importar as bibliotecas externas.

É muito fácil se perder no meio de tanta importação e na ordem do carregamento dos <i>scripts</i>. Pensando nisso, surgiram os module bundlers, que internamente constroi recursivamente um gráfico de dependências das importações, começando pelo arquivo principal (<i>entry point</i>), e processa toda a aplicação em pacote(s) JavaScript com todos os arquivos que sua aplicação precisa. Assim, com apenas uma linha de código, é possível importar toda a aplicação!

Ai vem a pergunta, mas e aqueles arquivos que não são JavaScript? Para isso temos os <i>loaders</i>, que permitem que esses arquivos sejam convertidos para módulos que o module bundlers consiga entender e adicionar no seu gráfico de dependências. Segue imagem ilustrando o processo:

![Module Bundler](/images/module-bundler.png)


### Material de apoio

[Webpack Documentation](https://webpack.js.org/concepts/)

[Uma História Web: A Origem dos Bundlers](https://medium.com/tableless/uma-hist%C3%B3ria-web-a-origem-dos-bundlers-40758347f1ef)

[Module Bundlers Explained... Webpack, Rollup, Parcel, and Snowpack](https://www.youtube.com/watch?v=5IG4UmULyoA)