# Otimização front-end

É importante que o site tenha um tempo de carregamento bom, mesmo que seja para mostrar um loading ou skeleton que é melhor do que uma página vazia. Para saber o quão otimizado é um site, podemos utilizar ferramentas como [Web Page Performance Test](https://www.webpagetest.org/) e [PageSpeed Insights](https://pagespeed.web.dev/?utm_source=psi&utm_medium=redirect&hl=pt-br) que, além de fazer a análise, nos da passos para podermos otimizar o site.

Abaixo seguem alguns pontos que podem ajudar na otimização, lembrando que cada situação precisa ser analisada, pesquisando mais a fundo seus pontos positivos e negativos.

## Minificação

O tamanho dos arquivos importam, pois o navegador vai ter que baixá-los para máquina que irá executar a aplicação. Basicamente, minificar é remover comentários, formatações, etc. O navegador não necessita dessas coisas para executar a aplicação, diminuindo o tamanho dos arquivos.

## Compressão do conteúdo

Comprimir arquivos no servidor ajuda na hora de baixar o conteúdo. Para saber o tamanho dos arquivos baixados e se estão zipados, basta olhar na aba network do devTools. Nessa aba temos o tamanho do conteúdo (size content) e o tempo que levou para ser baixado (timeline) e, ao clicar na requisição, podemos ver no header se temos alguma compressão (Content-Encoding).

Gzip e Brotli são exemplos de ferramentas para compressão de arquivos.

## Imagem

As imagens são uns dos maiores ofensores da performance, devido a falta de otimização e a quantidade de imagens e icones dos sites. Podemos fazer algumas mudanças simples que vão melhorar bastante esse aspecto, tais:

- Utilizar imagem do tamanho correto, lembrando que não é possível redimensionar svg.
- Utilize ferramentas de otimização de imagem para remover metadados (informações irrelevantes sobre a imagem) e diminuição da qualidade.

Além dessa melhoria, temos a técnica de sprite que consiste em gerar um único arquivo contendo várias imagens, ajudando a diminuir a quantidade de requisições.

## Script baixados

Acredito não ser um problema hoje em dia, pois muitos frameworks geram builds otimizadas. A quantidade de tag script no seu HTML influencia no tempo de carregamento, pois os navegadores paralelizam as requisições, então as próximas precisam esperar. Imagine que você tenha 20 script de CSS para serem baixados, pois você separou em vários arquivos e está importando um por vez, isso geraria 20 requisições para o servidor, o que poderia criar um gargalo. Ao invés disso, todos esses arquivos poderiam estar concatenado em um index.css e ter apenas uma requisição para baixar todo o estilo. Para isso podemos utilizar algumas ferramentas como [gulp-useref](https://github.com/jonkemp/gulp-useref) para concatenar e minificar o CSS. Isso vale também para os arquivos JavaScript.

Uma coisa que precisamos ter em mente ao fazer isso, é que você pode carregar arquivos que não serão utilizados em primeiro momento, para isso uma melhor solução é dividir os arquivos por contexto.

## Recursos inline

Para diminuir número de requisições ou fazer com que um recurso seja executado mais rápido, podemos usar o recurso inline, diretamente no HTML. Podemos tanto jogar o código dentro do arquivo HTML ou usar ferramentas de build que disponibiliza o código inline sem precisar colocar tudo no mesmo arquivo.

## Requisição Paralela

Os navegadores disponibilizam um número de conexões paralelas de acordo com o domínio, podemos aumentar esse número utilizando outro domínio para algumas requisições da nossa página. Por exemplo, se você estiver baixando algumas imagens do domínio <i>seu.dominio</i> e tiver outras baixando do domínio <i>outras.dominio</i>, essas requisições não irão disputar entre si e você terá o dobro de conexões paralelas, diminuindo as requisições na fila. Lembrando que não é aconselhável ter muitos domínios para não saturar a rede.

## Cache

O Cache possibilita que o navegador guarde dados da sua página para que ele não precise fazer novas requições quando tiver acessos novamente. Por padrão esse recurso vem desativado e o servidor precisa informar no header da requisição se o dado pode estar em cache, a duração do cache, entre outras coisas. [Esse link](https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching) explica como funciona o cache.

Vale lembrar que é preciso analisar quais arquivos fazem sentido estar em cache, normalmente arquivos estáticos são mais interessantes.

##  Javascript assíncrono

Deixar assíncrono scripts que não são essenciais para a primeira renderização da página, pode ajudar no tempo de carregamento, possibilitando mostrar algumas informações, melhorando a percepção de performance, antes que todos os scripts sejam baixado.

## Material de apoio

[Curso Performance Web I: otimizando o front-end](https://www.alura.com.br/curso-online-otimizacao-performance-web)

[HTTP Archive](https://httparchive.org/)

[Smart WebP, PNG and JPEG compression](https://tinypng.com/)

[SVG compression](https://jakearchibald.github.io/svgomg/)

[PNG Compression : 5 simple improvements](http://mainroach.blogspot.com/2013/09/png-compression-5-simple-improvements.html)

[CSS Sprites: What They Are, Why They’re Cool, and How To Use Them](https://css-tricks.com/css-sprites/.)

[Web Performance Otimization](https://wpostats.com/)