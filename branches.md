# Branch

Conceito de ramificação de projeto

## Criar ramificações do projeto

* Permite trabalhar de forma colaborativa
* Sempre haverá a branch principal

## Comandos para manipular branches

### Git Branch nome-da-branch

Cria uma nova branch, somente.
Ex: git branch feature/nome_da_feature

Para renomear a branch, add o parâmetro -m
Ex: git branch -m feature/novo_nome_da_branch

Para remover uma branch sem commit, add o parâmetro -d
Ex: git branch -d feature/novo_nome_da_branch

Para remover uma branch que possui commits e não foi mergeada, add o parâmetro -D
Ex: git branch -D feature/novo_nome_da_branch

### Git Checkout nome-da-branch

Altera a branch, somente.
Ex: git checkout feature/nome_da_feature

Cria a branch e altera o contexto, add o parametro -b
Ex: git checkout -b feature/nome_da_feature

### Git Merge nome-da-branch

Faz a junção do código da branch main com a branch em desenvolvimento trazendo todos os commits e criando um novo commit na branch principal.
Ex: git merge feature/nome_da_feature

### Git rebase nome-da-branch

Faz a junção do código da branch main com a branch em desenvolvimento trazendo todos os commits somente para a branch principal.
Ex: git merge feature/nome_da_feature

OBS: Não muito recomendado porque não respeita o histórico de alterações. Pode ser usado para trazer algum fix ou feature para uma branch de feature, mas não para unificar na branch principal.