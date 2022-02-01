# Otimização front-end

É importante que o site tenha um tempo de carregamento bom, mesmo que seja para mostrar um loading ou skeleton que é melhor do que uma página vazia. Para saber o quão otimizado é um site, podemos utilizar ferramentas como [Web Page Performance Test](https://www.webpagetest.org/) e [PageSpeed Insights](https://pagespeed.web.dev/?utm_source=psi&utm_medium=redirect&hl=pt-br) que, além de fazer a análise, nos da passos para podermos otimizar o site.

Abaixo seguem alguns pontos que podem ajudar na otimização, lembrando que cada situação precisa ser analisada, pesquisando mais a fundo seus pontos positivos e negativos.

## Minificação

O tamanho dos arquivos importam, pois o navegador vai ter que baixá-los para máquina que irá executar a aplicação. Basicamente, minificar é remover comentários, formatações, etc. O navegador não necessita dessas coisas para executar a aplicação, diminuindo o tamanho dos arquivos.

## Compressão do conteúdo

Comprimir arquivos no servidor ajuda na hora de baixar o conteúdo. Para saber o tamanho dos arquivos baixados e se estão zipados, basta olhar na aba network do devTools. Nessa aba temos o tamanho do conteúdo (size content) e o tempo que levou para ser baixado (timeline) e, ao clicar na requisição, podemos ver no header se temos alguma compressão (Content-Encoding). Os protocolos atuais já fazem essa compressão, inclusive do hearder da requisição.

Gzip e Brotli são exemplos de ferramentas para compressão de arquivos.

## Imagem

As imagens são uns dos maiores ofensores da performance, devido a falta de otimização e a quantidade de imagens e icones dos sites. Podemos fazer algumas mudanças simples que vão melhorar bastante esse aspecto, tais:

- Utilizar imagem do tamanho correto, lembrando que não é possível redimensionar svg.
- Utilize ferramentas de otimização de imagem para remover metadados (informações irrelevantes sobre a imagem) e diminuição da qualidade.

Além dessa melhoria, temos a técnica de sprite que consiste em gerar um único arquivo contendo várias imagens, ajudando a diminuir a quantidade de requisições.

## Número de requisições

É importante nos atentar a quantidade de requisições necessária para carregarmos os primeiros conteúdos e o tamanho dos arquivos que estamos baixando. Podemos priorizar algumas requisições e usar ferramentas que nos ajuda a pegar várias informações com apenas uma requisição, como [GraphQL](https://graphql.org/).

## Cache

O Cache possibilita que o navegador guarde dados da sua página para que ele não precise fazer novas requições quando tiver acessos novamente. Por padrão esse recurso vem desativado e o servidor precisa informar no header da requisição se o dado pode estar em cache, a duração do cache, entre outras coisas. [Esse link](https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching) explica como funciona o cache.

Vale lembrar que é preciso analisar quais arquivos fazem sentido estar em cache, normalmente arquivos estáticos são mais interessantes.

##  Javascript assíncrono

Deixar assíncrono scripts que não são essenciais para a primeira renderização da página, pode melhorar o tempo que demora para a página ficar utilizável. Sendo assíncrono, ele deixa de ser bloqueante, o que significa que o navegador não vai esperar baixar e executar aquele script para poder seguir com as outras requisições. Lembrando que como ele é assíncrono, não tem uma ordem para ser executado, assim deve ser analisado quais podem receber esse atributo.

Para fazer isso, basta colocar o atributo <i>async</i> na tag do script, assim:

`<script async src="path"></script> `

## Lazy load

É uma técnica que permite adiar alguns carregamentos de recurso, para melhorar o tempo de carregamento da página e evitar executar recursos desnecessários. Podemos ler mais sobre o assunto [aqui](https://developer.mozilla.org/en-US/docs/Web/Performance/Lazy_loading) e checar na documentação do [React](https://reactjs.org/docs/code-splitting.html) como fazemos para utilizar essa técnica para o carregamento dos componentes.

## Debounce e throttle

Essas técnicas são bem interessantes para utilizar com eventos do navegador ou alguma funcionalidade que dispara com muita frequência, seu intuito é diminuir processamento desnecessário.

A ideia das técnicas é bem semelhante, sendo o debounce para executar funções após um tempo sem o evento ser disparado, e o throttle determina o intervalo de tempo que a função deve ser chamada, sem precisar que o evento pare de ocorrer. O artigo [Debounce vs. Throttle no Javascript](https://blog.rocketseat.com.br/debounce-vs-throttle-no-javascript/) explica de forma mais detalhada.


## Preload CSS

O CSS é um recurso bloqueante, ou seja, o navegador espera baixar e executar antes de prosseguir com a renderização. Para evitar que o navegador espere todo o CSS, podemos utilizar a técnica de preload, que baixa os recursos, mas não bloqueia a renderização. [Nesse link](https://developer.mozilla.org/en-US/docs/Web/HTML/Link_types/preload) tem uma explicação mais detalhada.

## Material de apoio

[Curso Performance Web I: otimizando o front-end](https://www.alura.com.br/curso-online-otimizacao-performance-web)

[Performance Web II: Critical Path, HTTP/2 e Resource Hints](https://cursos.alura.com.br/course/performance-http2-critical-path)

[HTTP Archive](https://httparchive.org/)

[JPEG, GIF, PNG OR SVG - Which should You use?](https://dev.to/sarah_chima/jpeg-gif-png-or-svg---which-should-i-use-1o8o)

[Smart WebP, PNG and JPEG compression](https://tinypng.com/)

[SVG compression](https://jakearchibald.github.io/svgomg/)

[PNG Compression : 5 simple improvements](http://mainroach.blogspot.com/2013/09/png-compression-5-simple-improvements.html)

[CSS Sprites: What They Are, Why They’re Cool, and How To Use Them](https://css-tricks.com/css-sprites/.)

[Web Performance Otimization](https://wpostats.com/)

[Push do servidor HTTP/2](https://imasters.com.br/devsecops/push-do-servidor-http2)

[Performance Budget Calculator](https://www.performancebudget.io/)

[Browser Calories](https://browserdiet.com/calories/)

[The complete guide to lazy loading images](https://css-tricks.com/the-complete-guide-to-lazy-loading-images/)

[Virtualize grandes listas com janela de reação](https://web.dev/i18n/pt/virtualize-long-lists-react-window/)