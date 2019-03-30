# IntraChat

## Modulos de aplicacao

Permitindo o uso da aplicacao em diferentes projetos, a mesma e estruturada em dois modulos: Funcoes de chat e interface de interacao. Esses assim funcionam para permitir o uso de comandos simples para o chat, enquanto traz uma aplicacao de interface para rapida implementacao da aplicacao em outro projeto.

As funcoes de chat sao operacoes efetuadas a partir de classes que controlam os modulos do chat. Os modulos estabelecem os comandos basicos do chat, como enviar mensagem, receber mensagem, efetuar login e efetuar as operacoes de banco de dados. Assim, o mesmo estara separado entre funcoes publicas para operacoes diretas, como enviar mensagem, e funcoes privadas de operacoes indiretas, como sincronizar o banco de dados com a aplicacao.

A interface de interacao e um modulo de completa funcionalidade visual, ou seja, sao estruturas visuais predefinidas do chat, permitindo a rapida implementacao do mesmo em projetos previamente desenvolvidos. Essa parte e completamente opcional e pode ser interpretada ate mesmo como exemplo de implemetacao do modulo de funcoes de chat.

Por fora, ainda ha as configuracoes do sistema para seu bom funcionamento, como inicializacao do banco de dados e sincronizacao de dados entre aplicacao e banco. Este segue uma parte por fora dos outros dois modulos, sendo procedimento basico para bom funcionamento de ambos.

Desta forma, podemos estabelecer o seguinte fluxograma de dependencias da aplicacao:

> Instalacao || Inicializacao -> Funcoes de chat -> Interface de interacao

Assim, antes deve ocorrer a instalacao ou, caso ja instalado, a inicializacao do sistema, depois utilizada as funcoes de chat e, por ultimo, utilizada a interface de interacao com as funcoes de chat. Mas, como dito antes, Apenas as funcoes de chat ja bastam para o correto funcionamento da aplicacao e, por isso, a interface de interacao torna-se uma dependencia opcional ao uso.

-----

### Instalacao || Inicializacao

Este nao e um modulo gerenciado pelo usuario, mas e o primeiro a ser executado. Nessa primeira etapa, bancos de dados sao criados e inicializados ou apenas inicializados, caso ja existam. Posteriormente, esse estara responsavel pela sincronizacao dos dados locais da aplicacao com os dados do banco de dados. Por isso, as funcoes que ele exerce sao:

- Criacao do banco de dados
- Inicializacao do banco de dados
- Sincronizacao dos dados locais com os dados presentes no banco de dados

Assim, esse fica responsavel pela configuracao e estabilidade do sistema, funcionando totalmente escondido do usuario e apenas no servidor de aplicacao.

-----

### Funcoes de chat

O seguinte modulo e o principal modulo do projeto, pois com ele o usuario interage e efetua todos os comandos possiveis do sistema. Como esse e o principal modulo, ele possui as operacoes elementares da aplicacao, como login e envio de mensagem. Segue abaixo suas operacoes:

- Login de usuario
- Cadastro de usuario
- Enviar mensagem
- Carregar mensagem
- Alterar dados de usuario

Algumas das operacoes podem ocorrer de forma automatica ou ate mesmo nao serem publicas ao usuario.

-----

### Interface de interacao

O modulo de interface simplifica o uso da aplicacao a um caso visual que pode ser replicado e editado de maneira simples. Esse nao possui funcoes pre-estabelecidas, mas sim modulos de tela que podem ser replicados. Os modulos presentes sao:

- Cadastro de usuario
- Login de usuario
- Chat