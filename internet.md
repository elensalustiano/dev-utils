# Internet

Internet é uma rede global de computadores conectados que se comunicam através de protocolos.

## Hypertext Transfer Protocol (HTTP)

É um protocolo de comunicação para transferência de dados. O cliente requisita (request) dados para o servidor que responde (response). Segue alguns aspectos desse protocolo.

- Header: Contém informações importantes do contexto do cliente/servidor, como token, tipo de conteúdo, status da requisição, etc;
- Method: Chamado de verbo HTTP, indica a ação que o servidor deve fazer ao receber aquela requisição;
- Status code: É um código numérico, que o servidor envia para o cliente, que indica o estado da requisição. Temos os 5 principais grupos:
  - 1xx Informativo
  - 2xx Successo
  - 3xx Redirecionamento
  - 4xx Erro no cliente
  - 5xx Erro no servidor
- Body: Utilizado para transferir os dados. É nesse campo que colocamos os dados de formulários, recebemos os dados da usuária, etc.

## Hypertext Transfer Protocol Secure (HTTPS)

É uma extensão do protocolo HTTP com uma camada de segurança. O HTTPS ajuda a evitar ataques ao seu site, protegendo a privacidade das usuárias. É importante estar atento aos tipos de ataques, e com a ajuda da [OWASP](https://owasp.org/) (Open Web Application Security Project), uma comunidade online que produz insumo para segurança de sites, é possível utilizar ferramentas que ajudam a identificar vulnerabilidades. Abaixo seguem alguns exemplos de vulnerabilidades:

- Injection: É quando injetam um código que seu programa não estava esperando e ele executa.

https://sucuri.net/guides/owasp-top-10-security-vulnerabilities-2020/

## Domain Name System (DNS)

É o sitema que traduz nome de domínio para endereço IP, assim as pessoas não precisam memorizar IP e sim seu nome de domínio, que é mais fácil de lembrar.

## Material de apoio

[What is HTTP?](https://www.cloudflare.com/en-gb/learning/ddos/glossary/hypertext-transfer-protocol-http/)

[What is DNS? | How DNS works](https://www.cloudflare.com/en-gb/learning/dns/what-is-dns/)
