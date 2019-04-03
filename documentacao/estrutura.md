# IntraChat

## Estrutura de projeto

O projeto implementa dois modulos basicos: funcoes de chat e interface de interacao.

As funcoes de chat sao operacoes efetuadas a partir de classes que controlam os modulos do chat. Os modulos estabelecem os comandos basicos do chat, como enviar mensagem, receber mensagem, efetuar login e efetuar as operacoes de banco de dados. Assim, o mesmo estara separado entre funcoes publicas para operacoes diretas, como enviar mensagem, e funcoes privadas de operacoes indiretas, como sincronizar o banco de dados com a aplicacao.

A interface de interacao e um modulo de completa funcionalidade visual, ou seja, sao estruturas visuais predefinidas do chat, permitindo a rapida implementacao do mesmo em projetos previamente desenvolvidos. Essa parte e completamente opcional e pode ser interpretada ate mesmo como exemplo de implemetacao do modulo de funcoes de chat.

-----

## Enderecos e pastas

Sempre se baseando a partir da pasta raiz do projeto, toda a aplicacao esta presente na pasta _\\src\\_, incluindo tanto os componentes extras, como testes unitarios, como tambem os componentes principais do chat. Esses componentes principais se encontram nos diretorios _\\src\\public\\_ e _\\src\\resources\\_, sendo que, o primeiro gerencia os arquivos temporarios ou gerados pela aplicacao, como o chat, e o segundo possui as classes e arquivos principais do projeto.

Para melhor entendimento, esta e a estrutura de pastas:

- **IntraChat\\** - Raiz do projeto
  - **backup\\public\\** - Backup da pasta _\\src\\public\\_ gerenciado pelo FreeFileSync
  - **documentacao\\** - Documentacao em Markdown do projeto
  - **src\\** - Recursos do projeto
    - **public\\storage\\** - Arquivos temporarios ou gerados pela aplicacao
    - **resources\\** - Aplicacao
      - **class\\** - Classes do sistema
      - **js\\** - Javascripts do sistema
      - **styles\\** - Arquivos de estilo
        - **css\\** - CSS
        - **fonts\\** - Fontes
        - **img\\** - Imagens
      - **views\\** - Interfaces graficas
    - **tests\\** - Testes via PHPUnit
      - **feature\\** - Testes de grandes operacoes
      - **unit\\** - Testes de modulos unicos
    - **vendor\\** - Pacotes uteis ao sistema gerados via Composer

Alguns dos principais arquivos do projeto e suas funcionalidades:

- **\*.md** - Documentacao, em Markdown
- **.gitignore** - Configura arquivos ignorados pelo git
- **SyncSettings.ffs_gui** - Configuracao do FreeFileSync
- **composer.json** - Configuracao do Composer
- **phpunit.xml** - Configuracao do PHPunit
- **test.bat** - Executa os testes
- **.env** - Configuracao da aplicacao

Outros arquivos tambem podem surgir, como cache dos testes e arquivos resultantes do Composer.

-----

## Hierarquia de classes

O sistema possui diversas classes que operam sobre o todo, mas como o mesmo esta estruturado em um unico modulo de operacao do usuario, mais um complementar opcional para interface, o sistema possui a seguinte estrutura hierarquica:

> CRUD -> Gerenciador -> Operador -> Chat && Administrador

A classe pai, inicial, e o **CRUD** presente no seguinte [repositorio github](https://github.com/MateusBMP/CRUD). Este possui comandos simples de banco de dados previamente implementados que permitem a integracao da aplicacao com um banco de dados permitido pelo proprio CRUD. Desta forma, para mais informacoes sobre, leia a [documentacao](https://github.com/MateusBMP/CRUD/blob/master/documentacao/apresentacao.md) do mesmo.

Em seguida a classe **Gerenciador**, que expande a classe anterior agora com comandos de gerencia de arquivos locais, como leitura e escrita de arquivos. Esse efetuara as operacoes locais da aplicacao, gerenciando todos os arquivos locais do mesmo, sejam eles temporarios ou essenciais.

Agora segue-se pelo **Operador**, responsavel pelas operacoes que interligam o banco de dados aos arquivos locais. Ele e responsavel pelas operacoes gerais da aplicacao, como a sincronizacao dos arquivos locais com o banco de dados, por exemplo.

Por ultimo entram as classes usadas pelo usuario ou gerente do servidor: **Chat** e **Administrador**. Ambas sao independentes entre si pois ambas expandem a classe **Operador**, responsavel por toda interligacao dos comandos de banco de dados com os gerenciadores de arquivos locais. A primeira classe e utilizada pelo usuario e, consequentemente, pela interface de aplicacao opcional presente no projeto, enquanto a segunda fica a responsabilidade do gerente de servidor pois, enquanto a classe **Chat** efetua comandos de envio de mensagem, por exemplo, a classe **Administrador** realiza o backup das conversas no banco de dados da aplicacao de forma periodica.
