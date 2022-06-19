# Rentalk

## Objetivo

Este é uma aplicação em Nodejs de nivel esperimental, de um sistema de cadastro de carros.

## Arquitetura de Desenvolvimento

Código limpo é um conceito muito importante, isso representa dar nomes declarativos a constantes e funções, que decreve o que está acontecendo.

Código Limpo e SOLID são conteitos que pode definir o codigo limpo e organizado.



S => SRP - Single Responsability Principle(Principio da Responsabilidade Unica)

O => OCP - Open-Closed Principle (Principio aberto/fechado)

L => LSP - Liskey Substitution Principle (Principio da Segregação de Interface)

I => ISP - Interface Segregation Principle (Principio da Segregação de Interface)

D => DIP - Dependency Inversion Principle (Principio da Inversão de Dependencia)

## O que está sendo feito

1 - Inicialização do package.json

2- Instalação das libs 
express, 
ts-node-dev, 
typescript,
uuid

3- Incialização do tsc

4- Configuração de debug do codigo
`type: node`  `request: attach`  `skipFiles outFiles - mesmo nivel`

5- Criação da pasta de rotas separando as rotas da aplicação. Para cada recurso(dominio, de acesso como, cars, categories, images etc) sera criado uma rota.

6- Criação da pasta Model, que armazena as especificações de atributos e
tipos para a variavel. Seu formato é de classe e sua atribuição na categories.routes.ts é como tipagem.

7- Criação de Repositorios, especifico para o projeto trabalhado, este
é uma camada que será reponsavel por fazer toda a manipulação de dados.
Sendo responsavel por estruturar os dados, se conectar ao banco de dados,
fazer insert, delete, post.

8- Criar rota para exibição do que está sendo salvo(routes)

9- Tratamento de validação de dados para não passar categoria repetida.

10- Criar pasta Services, onde é repassado a responsabilidade, seguindo o principio do S do SOLID, fazendo a execução de validação e criação da categoria. Arquivo CreateCategoryService.ts, onde será definido também:
[x] - Definir o tipo de retorno
[x] - Alterar o retorno de error
[x] - Acessar o repositorio