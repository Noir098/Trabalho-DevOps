# Trabalho 1 - Changelog e Release com GitHub Actions

## Integrantes

- Nikolas Lodi Monteiro
- Lucas Dantas

## Sobre o projeto

Este repositório demonstra o uso de GitHub Actions para automatizar a documentação de alterações e a publicação de versões do projeto. Ele possui duas automações independentes: uma de changelog e uma de release.

## Action de Changelog

O workflow `changelog.yml` roda automaticamente a cada push na branch `main` (também pode ser executado manualmente pela aba Actions). Ele lê o histórico de commits com `git log` e monta uma lista com a data, a mensagem e o hash de cada commit. Essa lista é escrita na seção "Histórico de alterações" deste README, entre os marcadores do changelog. Depois, o `github-actions[bot]` faz um commit com a mensagem `docs: update changelog [skip ci]`, o que evita que o workflow rode em loop.

## Action de Release

O workflow `release-package.yml` roda quando uma tag de versão (ex: `v1.0.0`) é enviada ao repositório, ou manualmente pela aba Actions informando a versão. Ele compacta os arquivos do projeto (sem as pastas `.git` e `.github`) em um arquivo ZIP e usa a action `softprops/action-gh-release` para criar uma release na seção **Releases** do GitHub, anexando o ZIP e gerando automaticamente as notas da versão.

## Histórico de alterações

<!-- CHANGELOG:START -->
Aguardando a primeira execução do workflow...
<!-- CHANGELOG:END -->
