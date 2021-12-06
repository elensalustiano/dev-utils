# Acessibilidade (a11y)

Nos dias atuais, o uso da internet deixou de ser apenas passatempo, tornando-se uma ferramente que utilizamos para atividades importantes, sendo, as vezes, a única forma de acesso ao recurso.

Por esse motivo e vários outros, é cada vez mais importante pensarmos na inclusão digital. Temos alguns recursos na programação que facilita tornar um site mais acessível.

## HTML semântico

O HTML é a estrutura de uma página, nele definimos agrupamento de elementos, disposições, papel desempenhado, etc. Ou seja, organizamos como vamos oferecer um certo conteúdo.

O HTML semântico é a forma de deixar o site mais estruturado, assim como quando escrevemos um artigo e separamos nosso título por níveis, colocamos cabeçalho, rodapé, imagens com descrição, tabelas, etc. O HTML também fornece tags para elementos de acordo com o papel que será desempenhado, isso que o semântico quer dizer, utilizar tags certas para o tipo de estrutura que queremos construir.

Meu intuito não é entrar em detalhes sobre esse assunto, por isso vou deixar alguns materiais de apoio que recomendo a leitura.

## Leitores de tela

É importante comentar que pessoas com perda total de visão utilizam essas ferramentas para poderem navegar pelo site. Essas ferramentas leem informações do site para indicar possíveis ações (botões, links), ler textos, estruturas (titulo, tabela, gráfico, etc), entre outros.

Vou deixar um link de leitor [NVDA](https://www.nvaccess.org/).

## Tag de contéudo

No HTML temos tags que nos ajudam a definir e estruturar nossas páginas. O problema é que precisamos utilizar essas tags da melhor forma e nem todos planejam a estrutura do HTML, e isso é um grande problema para a acessibilidade. Mesmo que não seja priorizado outras questões de acessibilidade, apenas por criar uma estrutura semântica da página, já faz uma enorme diferença.

Vale ressaltar que HTML é para ser estrutural, questões de mudanças visuais devem ser tratadas no CSS (que também influência na leitura). O que quero dizer com isso, é que não utilizamos H1 pois queremos uma fonte maior, utilizamos porque queremos indicar que é um cabeçalho de nível 1, o mais importante daquele contexto.

### Tag lang

É o atributo que define o idioma que o leitor de tela vai ler seu site, isso é importante para a pronúncia das palavras e o sotaque. Quando precisar que alguma frase seja lida em um idioma diferente, é possível colocar o atributo lang na tag.

### Texto alternativo (alt)

É um texto que descrevemos uma imagem, caso ela não carregue, mostramos esse alt. Porém, ela é mais importante que isso, esse é o atributo lido pelos leitores de tela quando se depara com alguma imagem, por isso é importante sermos o mais descritivo possível. Caso a imagem não faça sentido ser lida, basta colocar o alt sem valor.

## Navegação por teclado

Precisamos pensar em como chegar em um certo conteúdo sem ser muito custoso, isso é importante porque algumas pessoas navegam utilizando o teclado e as vezes sem saber o quanto falta para chegar em um certo conteúdo. Sendo assim, é importante pensarmos em algumas coisas:

- Estrutura dos submenus, para que a navegação não fique muito complexa;
- Colocar link âncoras para pular navegação para algum conteúdo, esses links ficam visíveis apenas para leitores de tela ou navegação com tab;
- Roles (papel) e tags semânticas ajudam alguns leitores de tela a pular para conteúdo certo, facilitando navegação com atalhos;
- Esconder do leitor elementos apenas visuais (não agregam nada ao conteúdo, apenas design) para diminuir quantidade de elementos percorridos;
- Use readonly ao invés de disabled, pois dessa forma é possível navegar pelo elemento e ele será lido e informado que é apenas leitura; e
- Use label e atributo for para título de inputs, pois dessa forma o leitor sempre lê o nome e o valor do campo.

## WAI-ARIA ou ARIA

ARIA (Accessible Rich Internet Applications) tem o intuito de melhorar a semântica do HTML para aprimorar a acessibilidade, com recursos que nos ajuda a dar significado para a estrutura.

## Material de apoio

[Acessibilidade web parte 1: tornando seu front-end inclusivo](https://cursos.alura.com.br/course/acessibilidade-web-front-end)

[Você conhece HTML Semântico?](https://blog.geekhunter.com.br/voce-conhece-html-semantico/#O_que_e_HTML_semantico)

[HTML Semântico: Conheça os elementos semânticos da HTML5](https://www.devmedia.com.br/html-semantico-conheca-os-elementos-semanticos-da-html5/38065)

[WAI-ARIA – Estendendo o significado das interações](https://tableless.com.br/wai-aria-estendendo-o-significado-das-interacoes/)

[Introdução à ARIA para acessibilidade na Web](https://desenvolvimentoparaweb.com/miscelanea/aria-acessibilidade-web-a11y/)

[Acessibilidade - por que deixarmos de ser amadores para um público que espera mais de nós](https://pt.slideshare.net/MarinaDomingues7/acessibilidade-por-que-deixarmos-de-ser-amadores-para-um-pblico-que-espera-mais-de-ns)

[WebAIM, web accessibility in mind](https://webaim.org/)

[HTML5 Curso W3C Escritório Brasil](https://www.w3c.br/pub/Cursos/CursoHTML5/html5-web.pdf)

[Curso de HTML5 e CSS3](https://github.com/gustavoguanabara/html-css)

[CSS in Action - Invisible Content Just for Screen Reader Users](https://webaim.org/techniques/css/invisiblecontent/)

[Detectron2](https://github.com/facebookresearch/detectron2)

[Marcelo Sales, designer com foco em acessibilidade](https://medium.com/@msales)

[Awesome Accessibility](https://github.com/brunopulis/awesome-a11y)