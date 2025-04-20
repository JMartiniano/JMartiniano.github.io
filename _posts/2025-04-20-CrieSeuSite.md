---
title: "Criando Seu Próprio Site"
date: 2025-04-20 17:17:00 +0000
categories: [Dicas]
tags: [jekyll, chirpy, conhecimento]
---

## Para criar o seu próprio site, semelhante à este, você precisará de duas ferramentas:


1 - GitHub Pages\
2 - Jekyll

## Vamos aos Passos 

Comece criando um novo repositório no seu GitHub a partir do template oficial do tema Chirpy do Jakyll: [Template Jenkyll Chirpy](https://github.com/new?template_name=chirpy-starter&template_owner=cotes2020)

O nome do seu repositório deve ser igual ao seu usuário no GitHub, com o acrescimo do ".github.io". 

Por exemplo, seu seu usuario for "robertocarlos", o seu repositório deve receber o nome "robertocarlos.github.io" 

Tendo o seu repositório criado, no console web do GitHub acesse o seu respositório novo. 
Na aba "Settings" acesse a opção "Pages" e como opção de "Source" escolha "Deploy from a branch", abaixo selecione a branch principal do seu repositório, por padrão deve ser "main".

Como pasta de origem, selecione "root".

## Acessando seu Site

Você verá que o seu repositório já possui um tanto de arquivos, edite o seu arquivo "_config.yml", seguindo as instruções abaixo:


```
title: Meu Titulo
description: Descricao do meu site
lang: pt-BR
timezone: America/Sao_Paulo
url: "https://usuario.github.io"
baseurl: ""
```
Você pode pesquisar mais na internet sobre as possibilidades de edição do arquivo _config.yml, o céu é o limite.

Após alguns segundos (30 - 45) pesquise no seu navegador pelo site usuario.github.io, já deve ser possível ver a página padrão do Chirpy.

## Dica para personalizar seu Site 

Faça o clone do seu repositório, edite o arquivo _config.yml de acordo com as suas preferências e faça push das edições para ver as alterações no site.

Atenção:\
1 - Atente-se que o cache pode atrapalhar bastante na hora de ver as edições.\
2 - No seu repositório no console da GitHub, clique em "Action" e veja o andamento do deploy do seu site.

## Fazendo posts

Para fazer um post você deve criar um arquivo na pasta "_posts", o nome desse arquivo deve seguir um padrão: AAAA-MM-DD-nome-do-post.md

Com o arquivo criado, use a sintaxe padrão de arquivos md para escrever o seu artigo.

Por fim, publique o seu post novo fazendo o push e aguardando o deploy.