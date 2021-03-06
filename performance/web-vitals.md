# Web Vitals

> As Web Vitals são uma iniciativa do Google para fornecer orientação unificada em relação a sinais de qualidade essenciais que visam proporcionar uma ótima experiência ao usuário na web.


![Web vitals metrics](/images/web-vitals-metrics.png)

## Largest Contentful Paint (LCP)

 Informa o tempo de renderização da maior imagem ou bloco de texto visível na viewport em relação ao primeiro carregamento. [Clique aqui](https://web.dev/optimize-lcp/) para saber como otimizar essa métrica.

 A LCP é afetada principalmente por:
 - Tempos de resposta do servidor
 - Bloqueio de renderização por JavaScript e CSS
 - Tempos de carregamento de recursos
 - Renderização do lado do cliente

## First Input Delay (FID)

Informa a capacidade de resposta de uma página durante o carregamento, dedicando-se apenas aos eventos de clique, toque e pressionamento de tecla. Vale ressaltar que essa métrica mede apenas o "atraso" no processamento do evento, não mede o tempo de processamento do evento e nem o tempo que o navegador leva para atualizar a IU após a execução dos eventos. [Clique aqui](https://web.dev/optimize-fid/) para saber como otimizar essa métrica.

## Cumulative Layout Shift (CLS)

Informa a mudança de *layout* inesperado, quando algum elemento da tela muda sua posição inicial, devido ao carregamento assíncrono ou adição de elementos ao DOM acima do elemento existente. Essa métrica observa quanto conteúdo visível mudou dentro da janela de visualização e a distância em que os elementos impactados foram deslocados. [Clique aqui](https://web.dev/optimize-cls/) para saber como otimizar essa métrica.

Vale ressaltar que nem todas a mudanças de *layout* são ruim, desde que seja proposital e feita com alguma animação. É importante que a pessoa que utiliza perceba a movimentação e não acabe cometendo algum erro.
Para isso, propriedades como o *transform* do CSS permite animar elementos sem acionar mudanças de *layout*.

### Material de apoio

[Web Vitals - Essential metrics for a healthy site](https://web.dev/learn-web-vitals/)

[Largest Contentful Paint (LCP)](https://web.dev/lcp/)

[First Input Delay (FID)](https://web.dev/fid/)

[Cumulative Layout Shift (CLS)](https://web.dev/cls/)

[web-vitals library](https://github.com/GoogleChrome/web-vitals)