---
layout: post
title:  "ng-fabrica"
date:   2014-11-11
categories: fabrica
---

# Objetivos: 

- familiarizar conceitos:
	- data binding
	- directives
	- scopes and controllers



# Dependency injection 

- estabelecer relação de dependência entre módulos não por meio estático (código)
mas de modo dinâmico. 
- premite "mock" das dependências de um determinado módulo, o que possibilita testes
unitátios


# Testes unitários:
- lidar com $scope ao invés de lidar diretamente com interface dá mais controle



# Directives

## ng-repeat

- Repete o bloco de 

# Formulários:

## ng-model

- declara a relação entre o campo de input e o escopo.
- define qual é o dado que o input manipula.

## ng-



PONTOS INTERESSANTES A SEREM DEMONSTRADOS:

- data-binding
- filters
- form validation (pristine, dirty, valid, invalid)
- ng-class



AFAZERES:
- APRENDER IONIC ROUTING SYSTEM.
- IONIC:
	- modals







# 1: instalação do ambiente de desenvolvimento

## Instalação de:
	node -> http://nodejs.org
	ionic -> sudo npm install -g ionic
	gulp -> sudo npm install -g gulp
	// (remover cache de super user -> sudo rm -rf ~/.npm)

## Start do projeto
	ionic start {{nome_do_projeto}} [blank|tabs|sidemenu]
	cd {{nome_do_projeto}}
	ionic serve

# 2: conceitos [parte1]

## Controlador (controller)

- Aumenta o escopo definindo métodos disponíveis no escopo
- Os métodos definidos no controller são transferidos para o escopo e ...
- por isso estarão disponíveis para serem acessados por expressões
nos templates do angular.

## Diretiva (directive)

- declaração no html que indicam as ações e responsabilidades que cada bloco da interface tem
- via atributos das tags html: 
	- declara a controller:
		<div ng-controller="ExampleController"></div>
	- declara o atributo do escopo controlado pelo campo de input: 
		<input ng-model="person.name" type="text">
- via novas tags html:
	- declara a intenção de utilizar um bloco de código custom do ionic:
		<ion-sidemenu>
			<ion-content>
			</ion-content>
			<ion-side left>
			</ion-side>
		</ion-sidemenu>


## Escopo ($scope)

- "Area de operação"
- Objeto JS que contém a camada de dados da aplicação ou do bloco da aplicação.
- Herança de escopos

[ por trás: objetos JS encadeados por prototype ]

## Expressões (expressions)

- valores a serem avaliados pelo processador de expressões do angular.
- todas as expressões são avaliadas dentro de algum escopo

	<div>{{ person.name }}</div>
	<ul>
		<li ng-repeat="person in people">
			<img src="{{ person.picture }}">
			<div>{{ person.name | lowercase }}</div>
		</li>
	</ul>


## Dependency injection 

- estabelecer relação de dependência entre módulos não por meio estático (código)
mas de modo dinâmico. 
- premite "mock" das dependências de um determinado módulo, o que possibilita testes
unitátios
