RELATÓRIO TÉCNICO

Desenvolvimento de Aplicação Web CRUD - Projeto de Estoque de rações com
Laravel

Autores:
Arthur Pontes Labre Feitosa e Nadima Julia Suterio de Oliveira

1. Introdução
   
Este relatório apresenta o processo completo de desenvolvimento de uma aplicação web
construída com o framework Laravel, seguindo o padrão CRUD (Create, Read, Update,
Delete). O objetivo do projeto foi implementar um sistema funcional de gerenciamento de
dados, utilizando boas práticas de programação, organização de código e arquitetura MVC
(Model–View–Controller).
A aplicação desenvolvida foi um sistema de gerenciamento de rações, contendo:
● Cadastro de rações
● Edição de rações
● Listagem de rações
● Exclusão de rações
● Página inicial personalizada
● Tela de configurações
Todo o código foi construído, revisado e corrigido ao longo do processo.

2. Processo de Desenvolvimento

A seguir, descrevo as etapas adotadas para implementar cada parte do CRUD.
2.1. Configuração Inicial do Projeto
1. Criação do projeto Laravel
2. Configuração do banco de dados no arquivo .env
3. Teste da conexão com php artisan migrate
2.2. Criação da Estrutura do CRUD
2.2.1. Model e Migration
Criamos o model Racao e sua migration:
A migration definiu os campos:
● nome
● marca
● quantidade
● preco
● tipo
Após isso, executamos:
2.2.2. Controller
Criamos o controller principal:
Ele contém os métodos:
● index() → listar
● create() → exibir formulário
● store() → salvar novo registro
● edit() → exibir formulário de edição
● update() → atualizar registro
● destroy() → excluir registro
2.2.3. Rotas
No arquivo routes/web.php, configuramos:
Essa única linha cria automaticamente todas as rotas do CRUD.
Também adicionamos:
E criamos as rotas de configurações:
2.2.4. Views
Criamos as views dentro de:
As principais telas foram:
● index.blade.php → listagem
● create.blade.php → formulário de cadastro
● edit.blade.php → formulário de edição
Também criamos:
● home.blade.php → página inicial com cards
● configuracoes/index.blade.php → tela de configurações
Todas as telas utilizam o layout:

3. Desafios e Soluções
   
Durante o desenvolvimento, alguns desafios surgiram. Abaixo estão os principais e como
foram resolvidos.
3.1. Organização das Rotas
Desafio: As rotas estavam desorganizadas e algumas foram inseridas no meio do arquivo,
causando confusão.
Solução: Reorganizamos o arquivo web.php, colocando todos os use no topo e
agrupando rotas por funcionalidade.
3.2. Página Inicial em Branco
Desafio: A página inicial aparecia vazia devido à ausência da view home.blade.php.
Solução: Criamos a view e configuramos corretamente a rota /.
3.3. Tela de Configurações sem Conteúdo
Desafio: A tela de configurações aparecia totalmente branca.
Solução: Criamos a view configuracoes/index.blade.php e garantimos que o
controller retornasse a view correta.
3.4. CRUD Incompleto
Desafio: Algumas partes do CRUD estavam faltando (views, métodos, rotas).
Solução: Implementamos todas as partes do CRUD seguindo o padrão Laravel Resource
Controller.
Recursos e Ferramentas Utilizados
Durante o desenvolvimento, utilizamos:
Laravel Framework
● Estrutura MVC
● Artisan CLI
● Rotas automáticas com Route::resource
● Blade Templates
Bootstrap
● Estilização das telas
● Layout responsivo
● Botões, tabelas e cards
Git e GitHub
● Controle de versão
● Publicação do projeto
● Histórico de alterações
VS Code
● Editor principal
● Extensões para PHP e Laravel
MySQL
● Banco de dados relacional
● Armazenamento das informações

4. Conclusão
   
O projeto permitiu desenvolver uma aplicação web completa utilizando Laravel, aplicando
conceitos fundamentais como:
● Estrutura MVC
● CRUD completo
● Organização de rotas
● Controllers e Models
● Views com Blade
● Layouts reutilizáveis
● Boas práticas de desenvolvimento
Além disso, o processo proporcionou experiência prática na resolução de problemas,
organização de código e uso de ferramentas modernas de desenvolvimento.
O sistema está funcional, organizado e pronto para ser expandido com novas
funcionalidades.
