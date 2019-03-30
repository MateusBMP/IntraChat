# IntraChat

## Estrutura de projeto

O projeto implementa dois modulos basicos: funcoes de chat e interface de interacao.

As funcoes de chat sao operacoes efetuadas a partir de classes que controlam os modulos do chat. Os modulos estabelecem os comandos basicos do chat, como enviar mensagem, receber mensagem, efetuar login e efetuar as operacoes de banco de dados. Assim, o mesmo estara separado entre funcoes publicas para operacoes diretas, como enviar mensagem, e funcoes privadas de operacoes indiretas, como sincronizar o banco de dados com a aplicacao.

A interface de interacao e um modulo de completa funcionalidade visual, ou seja, sao estruturas visuais predefinidas do chat, permitindo a rapida implementacao do mesmo em projetos previamente desenvolvidos. Essa parte e completamente opcional e pode ser interpretada ate mesmo como exemplo de implemetacao do modulo de funcoes de chat.

-----

## Enderecos e pastas

Sempre se baseando a partir pasta raiz do projeto, toda a aplicacao esta presente na pasta _\\src\\_, incluindo tanto os componentes extras, como testes unitarios, como tambem os componentes principais do chat. Esses componentes principais se encontram nos diretorios _\\src\\public\\_ e _\\src\\resources\\_, sendo que, o primeiro gerencia os arquivos temporarios ou gerados pela aplicacao, como o chat, e o segundo possui as classes e arquivos principais do projeto.

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

Outros arquivos tambem podem surgir, como cache dos testes e arquivos resultantes do Composer.