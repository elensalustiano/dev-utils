# Gerenciador de pacotes (package manager)

Antigamente, para utilizar pacote de funcionalidade distribuída (3rd party packages), era necessário baixar o pacote e fazer o importe no HTML com a tag <i>script</i>. Esse trabalho era muito manual e custoso, e é ai que entra os gerenciadores de pacotes.

O gerenciador de pacotes baixa todas as nossas dependências, criando uma pasta para armazena-lás, e nos ajuda a mante-lás atualizadas. Além, de nos ajudar com outras coisas, tais:

- Encontrar os pacotes corretos;
- Checar vulnerabilidades e atualizações;
- Baixar e salvar em um local apropriado;
- Gerenciar sub dependências;

No JavaScript, basicamente é necessário apenas um arquivo para fazer todo esse gerenciamento. Nesse arquivo, chamado <i>package.json</i>, colocamos todas as dependências e, ao rodar o comando de instalar, todos os pacotes são baixados e salvos na máquina, sem precisar fazer o versionamento de todos os pacotes.

### Material de apoio

[Package management basics](https://developer.mozilla.org/en-US/docs/Learn/Tools_and_testing/Understanding_client-side_tools/Package_management)

[NPM - package manager](https://docs.npmjs.com/)

[Yarn - package manager](https://classic.yarnpkg.com/en/docs/getting-started)