---
title: "Lição 12 - Implante o site com o GitHub Pages"
description: "Configure um fluxo de trabalho do Pages com o aplicativo GitHub Copilot, revise a pull request e verifique o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Dê ao Space Quiz um endereço público implantando-o com o GitHub Pages. O Copilot pode preparar o fluxo de trabalho e orientar a implantação, mas você continua responsável por revisar as alterações e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot que configure a implantação no GitHub Pages;
- revisar o fluxo de trabalho e a pull request antes de fazer o merge;
- acompanhar a implantação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas ainda é preciso oferecer uma maneira simples de testá-lo. Publicar o site de um único arquivo com o GitHub Pages o torna acessível por uma URL pública, sem adicionar um servidor ou dependência de runtime.

## Peça ao Copilot para implantar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama de três etapas: uma pull request do space-quiz mesclada; uma execução bem-sucedida de Deploy website no GitHub Actions com as etapas Build website, Upload artifact e Deploy to Pages; e o Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede que o agente crie e faça merge de uma pull request e altere as configurações do Pages do repositório. Revise o diff, as permissões de implantação e todas as solicitações de aprovação do GitHub antes de continuar.

## Revise o fluxo de trabalho e verifique a implantação

1. Confirme que o README só foi adicionado se o repositório ainda não tinha um.
2. Revise as alterações da pull request, incluindo as etapas de build e implantação do fluxo de trabalho.
3. Faça o merge somente depois que as verificações obrigatórias da pull request forem aprovadas.
4. Acompanhe a execução de implantação do GitHub Actions até que seja concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz carrega.

Se o agente não puder habilitar o Pages ou fazer o merge da pull request, siga as instruções específicas fornecidas. Não considere a tarefa concluída até que a implantação seja bem-sucedida e o site publicado carregue.

## Resumo e próximos passos

O Space Quiz está no ar, e você verificou a implantação em vez de confiar apenas no relato do agente. Continue para a [lição 13: revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
