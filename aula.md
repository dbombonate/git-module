# Repo git para Projetos de infra, software, conjunto de código

## Config necessária para iniciar o repo git:

* Username;
* Email;
* Editor de texto padrão;
* Nome da Branch padrão.

Comandos para verificar:
'git config --list

Config Username
'git config --global user.name "Seu User"

Config Email
'git config --global user.email seuuser@email.com

Config editor de texto padrão
'git config --global core.editor vim # pode ser outro editor

Config Branch padrão
'git config --global init.defaultBranch main

## Escopo de config:

Global: --global -> nível de usuário. Armazenada em /home/user/.gitconfig
System: --system -> nível de máquina. Aplica a config para qualquer usuário que utilize o git na máquina use aquela config.
Project: --project -> nível de projeto. Aplica a config para qualquer usuário que utilize o git no projeto use aquela config.

#### Herança do escopo: Project -> System -> Global

## Estado dos arquivos no GIT

### UNTRACKED File

Indica que o arquivo não está sendo monitorado pelo git, não está sendo controladas as alterações realizadas nesse arquivo.

### Staged File

Indica que o arquivo está em uma área intermediária entre o untracked e o commit. Ainda não está sendo rastreado.

### Unmodified File

Indica que o arquivo monitorado não foi modificado.

### Modified File

Indica que o arquivo monitorado foi modificado.

## Comandos GIT

### Git Status

Mostra o estado do repositório.

### Git Add

Adiciona arquivo, ou arquivos para área de Stage.
Ex: git add nome_do_arquivo

### Git rm

Remove arquivo, ou arquivos da área de Stage.
Ex: git rm nome_do_arquivo

### Git commit

Cria um snapshot do arquivo, uma cópia daquele momento do estado do arquivo.
Ex: git commit -m "Mensagem do commit"
    git commit -a -m "Mensagem do commit" -> Remove a necessidade de dar um git add antes do commit

### Git log

Permite verificar o histórico de alterações realizadas na branch ou em arquivos especificos.
Ex: git log
    git log -p <nome_do_arquivo>

### Git reset
Permite remover alterações nos arquivos com base nos commits.
Ex: git reset --soft HEAD~1 -> Remove o commit e deixa o arquivo no estado de modificado
    git reset --hard -> Volta o arquivo ou arquivos para o último commit válido

### Git tag
Usado para criar marcos no projeto, criar versões do projeto entregue.
Ex: git tag -a <nome_da_tag> -m "MSG_PARA_CRIAR_A_TAG"
    git tag -a <nome_da_tag> -m "MSG_PARA_CRIAR_A_TAG" <hash_do_commit_marco> -> Criar tag após a existência de outra tag
    git tag -d <nome_da_tag> -> Deletar tag