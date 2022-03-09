# Navegadores

Para podermos fazer algumas melhorias de performance no nosso site, precisamos entender alguns aspectos de funcionamento do navegador.

## Estrutura de alto nível

O navegador tem alguns componentes principais, são eles:
 - User interface: É a parte visual do navegador, como a barra de favorito, barra de endereço, botões, etc.
 - Browser engine: Responsável por manipular os dados enviados pela user interface e mandar para a rendering engine.
 - Rendering Engine: Responsável por renderizar o conteúdo, fazendo as manipulações necessárias de acordo com a tecnologia utilizada.
 - Networking: Cuida de todos os aspectos relacionados a internet, como protocolos, seguranças, etc.
 - UI backend: Utiliza de operações do sistema para mostrar widgets.
 - JavaScript interpreter: Analisa e executa códigos JavaScript.
 - Data Persistence: Utilizada para salvar dados localmente. E nessa camada que encontramos localStorage, IndexedDB, FileSystem, Cache, etc;

Segue ilustração dessa estrutura:

![Estrutura do navegador](/images/browser-structure.png)

### Rendering engines

Responsável por renderizar conteúdos que são, normalmente, HTML, XML e imagens. Nem todos os navegadores usam a mesma engine, temos: Internet Explorer com a Trident, Firefox com a Gecko, Safari com a WebKit, Chrome and Opera com a Blink.

// TODO
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

[How Browsers Work: Behind the scenes of modern web browsers](https://www.html5rocks.com/en/tutorials/internals/howbrowserswork/)

[How does web browsers work?](https://medium.com/@monica1109/how-does-web-browsers-work-c95ad628a509)