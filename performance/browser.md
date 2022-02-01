# Navegadores

Para podermos fazer algumas melhorias de performance no nosso site, precisamos entender algumas coisas que o navegador faz a partir do momento que requisitamos um site.

## caminho de renderização crítico

Alguns recursos são críticos para que o navegador comece a desenhar um site, o primeiro é o HTML principal, onde colocamos os recursos iniciais que precisam ser baixados para a renderização. Normalmente encontramos nesse arquivo alguns scripts e CSS que determinam como nosso página será desenhada, por esse motivo esses recursos são considerados bloqueantes. A imagem abaixo exemplifica esse fluxo:

![Web vitals metrics](/images/critical-rendering-path.jpg)

Analisando a imagem, primeiro o navegador obtém o HTML e constrói o DOM (Document Object Model). Após isso, ele procura por JavaScript e CSS que são recursos que influenciam diretamente no layout e começa a baixar. O arquivos de CSS também precisam ser interpretados, chamamos de CSSOM (CSS Object Model), semelhante ao processo de construção do DOM, onde as regras dos elementos são definidas.

Com todas as informações principais carregadas, ele começa a desenhar o site, temos essas 3 principais etapas:

1. Render Tree: Nessa etapa temos a combinação do DOM e CSSOM, onde obtemos os conteúdos e seus estilos;
2. Layout: Nessa etapa o navegador calcula os tamanhos e posições dos elementos visíveis. Esse processo é disparado sempre que o Render Tree é atualizado ou algum tamanho de elemento muda; e
3. Paint: Nessa etapa os elementos são desenhados.

Com isso notamos que não podemos apenas nos preocupar com o tempo de carregamento do HTML, se ele depende do CSS e JS para continuar o processo. Além disso, vale lembrar que a ordem dos scripts no HTML define sua prioridade na hora de baixar, por isso é importante manter o CSS no topo e colocar os scripts no final do arquivo após o conteúdo (body), dessa forma o JS será baixado após todo o resto do conteúdo.

## Material de apoio

[Performance Web II: Critical Path, HTTP/2 e Resource Hints](https://cursos.alura.com.br/course/performance-http2-critical-path)

[Understanding the critical rendering path, rendering pages in 1 second](https://medium.com/@luisvieira_gmr/understanding-the-critical-rendering-path-rendering-pages-in-1-second-735c6e45b47a)

[Critical Rendering Path - Velocidade também é uma funcionalidade](https://www.infoq.com/br/presentations/critical-rendering-path/)

[Desempenho da renderização](https://developers.google.com/web/fundamentals/performance/rendering)

[CSS triggers](https://csstriggers.com/)

