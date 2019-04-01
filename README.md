# IntraChat

[![versao](https://img.shields.io/github/tag-date/mateusbmp/intrachat.svg?color=light&label=versao)](https://github.com/MateusBMP/IntraChat) [![PHP minimo](https://img.shields.io/badge/php-%5E7.2-blue.svg)](http://www.php.net) [![licenca](https://img.shields.io/github/license/mateusbmp/intrachat.svg?label=licenca)](https://github.com/MateusBMP/IntraChat/blob/master/LICENSE)

## Apresentacao

O **IntraChat** e um chat de texto em PHP, usando banco de dados para documentar as conversas e validar o usuario, enquanto estabelece comunicacao via aplicacao entre os usuarios. Sua estrutura visa a aplicacao em diferentes projetos e, desta forma, possui uma estrutura flexivel e de mais simples configuracao possivel.

Sua documentacao foi inteiramente escrita usando [Markdown](https://markdownguide.org).

Para mais detalhes sobre a documentacao do projeto ou como colaborar como mesmo, acesse o diretorio _[documentacao](https://github.com/MateusBMP/IntraChat/blob/master/documentacao)_ na raiz do projeto.

-----

## Procedimento basico

A aplicacao foi desenvolvida para funcionar tanto localmente quanto em um servidor de aplicacao e, por isso, exige ser configurado e instalado antes de ser usado. Para isso, siga o seguinte protocolo:

- Criar aquivo _.env_ de acordo com arquivo de referencia _.env.example_
- Configurar arquivo _.env_ de acordo com as necessidades da aplicacao
- Importar a classe _Administrador_ e executar a funcao **instalar**

O arquivo _.env_ armazena informacoes essenciais a aplicacao, como parametros de conexao ao banco de dados e tipo de banco usado. Desta forma, esse arquivo nao deve ser incorporado ao corpo do codigo que sera compartilhado, a nao ser que se possua confianca ao transmitir esses dados.

Apos criar o arquivo _.env_, edite pelo menos as variaveis de banco de dados, ou seja, as que comecam com **BD_**.

Por ultimo, execute a funcao **instalar** presente na classe _Administrador_. Essa criara os arquivos basicos da aplicacao, como o chat e o banco de dados. Para mais informacoes em como executa-la, leia a [documentacao](https://github.com/MateusBMP/IntraChat/documentacao/classes/administrador.md) da classe.

Quando desejar ativar o servidor, execute a funcao **ativar** presente na classe _Administrador_. Quando desejar desativar o servidor, execute a funcao **desativar** tambem presente na mesma classe.

Agora, para que o cliente use a aplicacao, use a classe _Chat_ ou a propria interface fornecida. As interfaces fornecidas se encontram do diretorio _src/resources/views_, sendo elas:

- **login.php**
- **cadastrar.php**
- **chat.php**

-----

## Desenvolvedores

- [Mateus Pereira](https://github.com/MateusBMP)
- [Jadde Freitas](https://github.com/Jaddefreitas)
- [Erycles Silva](https://github.com/EryclesIc)