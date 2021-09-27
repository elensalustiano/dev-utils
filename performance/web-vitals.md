# Web Vitals

> As Web Vitals são uma iniciativa do Google para fornecer orientação unificada em relação a sinais de qualidade essenciais que visam proporcionar uma ótima experiência ao usuário na web.

## Largest Contentful Paint (LCP)

 informa o tempo de renderização da maior imagem ou bloco de texto visível na viewport em relação ao primeiro carregamento. [Clique aqui](https://web.dev/optimize-lcp/) para saber como otimizar essa métrica.

 A LCP é afetada principalmente por:
 - Tempos de resposta do servidor
 - Bloqueio de renderização por JavaScript e CSS
 - Tempos de carregamento de recursos
 - Renderização do lado do cliente

## First Input Delay (FID)

Informa a capacidade de resposta de uma página durante o carregamento, dedicando-se apenas aos eventos de clique, toque e pressionamento de tecla. Vale ressaltar que essa métrica mede apenas o "atraso" no processamento do evento, não mede o tempo de processamento do evento e nem o tempo que o navegador leva para atualizar a IU após a execução dos eventos. [Clique aqui](https://web.dev/optimize-fid/) para saber como otimizar essa métrica.

### Referência
[Web Vitals - Essential metrics for a healthy site](https://web.dev/learn-web-vitals/)

[Largest Contentful Paint (LCP)](https://web.dev/lcp/)

[First Input Delay (FID)](https://web.dev/fid/)