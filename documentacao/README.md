# IntraChat

## Apresentacao

O **IntraChat** e um chat de texto em PHP, usando banco de dados para documentar as conversas e validar o usuario, enquanto estabelece comunicacao via aplicacao entre os usuarios. Sua estrutura visa a aplicacao em diferentes projetos e, desta forma, possui uma estrutura flexivel e de mais simples configuracao possivel.

O projeto possui testes simples, usando o PHPUnit, que podem ser encontrados no diretorio _\\src\\tests\\_ e foi desenvolvido em Windows 10.

Sua documentacao foi inteiramente escrita usando [Markdown](https://markdownguide.org).

-----

## Executando o sistema

Usando o [XAMPP](https://www.apachefriends.org) e posicionando as pastas _\\src\\public\\_ e _\\src\\resources\\_ do projeto no diretorio _\\htdocs\\IntraChat\\_, no diretorio raiz do XAMPP, pode-se acessar a pagina inicial pelo endereco:

- <http://localhost/IntraChat/resources/views/index.php>

Para executar os testes, execute o seguinte comando via terminal (Windows) no diretorio _\\src\\_ do projeto:

- ``$ .\test.bat``

-----

## Configurando o sistema

O projeto foi estruturado em um diretorio especifico na raiz do Windows e, por isso, recomenda-se, principalmente se utilizando o [FreeFileSync](https://freefilesync.org), sua criacao no diretorio _C:\\dev\\IntraChat\\_. Isso serve para uso completo do projeto pois, se usando somente os componentes basicos do mesmo, apenas leve em consideracao a versao do PHP exigida nos requisitos de sistema e basta usar os diretorios _\\src\\resources\\_ e _\\src\\public\\_ na raiz do projeto.

Arquivos executaveis nao podem ser enviados para algumas pastas ou, por questoes de seguranca, nao sao compartilhados, por isso, no diretorio _\\src\\_ do projeto, deve-se executar o seguinte comando:

- ``$ composer update``

Se necessario, use o comando ``composer install`` no lugar do comando ``composer update``. Esses comandos inserem as bibliotecas minimas a boa implementacao do projeto, como o [PHPUnit](https://phpunit.de), no diretorio _\\src\\_ seguindo a partir da raiz do projeto.

Para executar testes de forma facil, ou caso esteja com problemas em usar os comandos padroes do PHPUnit, ou seja, usando o comando ``.\test.bat``, crie, se necessario, este mesmo arquivo no diretorio _\\src\\_, contendo as seguintes linhas de codigo:

> ``vendor/bin/phpunit``

O FreeFileSync facilita o processo de sincronizacao do projeto com suas diferentes pastas, como no diretorio _\\htdocs\\_ do XAMPP. Para seu bom funcionamento, se necessario, deve-se criar as seguintes pastas:

- _\\backup\\_ dentro do diretorio do projeto
- _\\htdocs\\IntraChat\\_ dentro do diretorio do XAMPP

-----

## Documentacao

O projeto possui uma vasta documentacao explicando sua estrutura, funcionalidades e aplicacoes. Para melhor entende-la, eis os arquivos de documentacao presentes:

- classes/
  - **Administrador**: Explica as funcoes da classe _Administrador_
- **Estrutura**: Explica a estrutura do projeto, descrevendo suas principais pastas e utilidades de cada uma
- **Modulos**: Apresenta os modulos de uso da aplicacao e suas principais operacoes de forma resumida
- **README**: Arquivo atual, apresentando a base do projeto, como configura-lo e como executa-lo
- **Requisitos**: Requisitos minimos e opcionais para o bom funcionamento ou implementacao do projeto