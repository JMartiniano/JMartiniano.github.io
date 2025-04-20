---
title: "Criando Seu Próprio Site"
date: 2025-04-20 17:17:00 +0000
categories: [Dicas]
tags: [jekyll, chirpy, conhecimento]
---

# Para criar o seu próprio site, semelhante à este, você precisará duas ferramentas:

1 - GitHub Pages\
2 - Jekyll

## Vamos aos Passos 

Comece criando um novo repositório a partir do template oficial do tema Chirpy do Jakyll: https://github.com/new?template_name=chirpy-starter&template_owner=cotes2020 \

O nome do seu repositório deve ser igual ao seu usuário do GitHub, com o acrescimo do ".github.io". por exemplo: usuario.github.io\

Tendo o seu repositório criado, no console web do GitHub acesse o seu respositório novo. Na aba "Settings" acesse a opção "Pages" e como opção de Source escolha "Deploy from a branch", abaixe selecione a branch principal do seu repositório, por padrão deve ser "main".\

Como pasta de origem, selecione "root".\

## Acessando seu Site

Edite o seu arquivo _config.yml para algo como o exemplo abaixo:

'''
title: Meu Titulo
description: Descricao do meu site
lang: pt-BR
timezone: America/Sao_Paulo
url: "https://usuario.github.io"
baseurl: ""
'''

Após alguns segundos (30 - 45s) pesquise no seu navegador pelo site usuario.github.io, já deve ser possível ver a página padrão do Chirpy.

## Dica para personalizar seu Site 

Faça o clone do seu repositório, edite o arquivo _config.yml de acordo com as suas preferências e faça push das edições para ver as alterações no site.\

Atenção:\
1 - Atente-se que o cache pode atrapalhar bastante na hora de ver as edições.\
2 - No seu repositório no console da GitHub, clique em "Action" e veja o andamento do deploy do seu site.