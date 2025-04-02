---
layout: post
title: "Listar arquivos modificados em uma branch no git"
date:   2025-04-01 23:45:00 -0300
categories: dev git
---

Meus caros,

Às vezes, preciso saber quais arquivos foram modificados na branch atual em comparação com outra branch. 

É bem simples, basta fazer checkout na branch que você deseja (por exemplo, `branch-feature`)

```console
git checkout branch-feature
```
e então verificar as difereças em relação a branch de comparação (por exemplo, a branch `main`) 

```console
git diff --name-only main
```

O parâmentro --name-only retorna apenas o nome do arquivo com seu caminho.

Aproveitando, se quiser saber os arquivos modificados em um commit, faça 

```console
git diff-tree --no-commit-id --name-only -r <id-do-commit>
```

A Paz,
=)