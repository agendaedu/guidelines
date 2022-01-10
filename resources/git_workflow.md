Git Workflow
============

## Criação de Branches

Nós seguimos alguns padrões para criação de branches que são relacionados com o nosso fluxo de
desenvolvimento do Jira, portanto, antes de ler esse guideline leia [Fluxo de trabalho](https://github.com/agendakids/guidelines/blob/main/resources/workflow.md).

Abaixo está a explicação de cada tipo de branch que temos no momento:

- Branch principal: nossa branch principal é a `master`, nós assumimos que todo código
mesclado na `master` já foi revisado, testado e está pronto para ser enviado para produção.
- Epics: cada epic deverá ter uma branch que tem como base a `master`, seu nome deve seguir
o seguinte padrão `epic/[código da epic]`, por exemplo `epic/se-1234`.
- Tasks: tasks também devem ter suas branches, podendo ter como base a `master` ou alguma epic,
em todos os casos, seu nome deve seguir o padrão `[tipo da task]/[código da task]`, por exemplo
`feature/se-1234`, `bug/se-1234`, `techtask/se-1234`, etc.
- Extra: branches de modificações que não tem relação com a sua sprint devem ser criadas seguindo
o padrão `extra/[sua modificação]`, por exemplo `extra/update_jest`.


## Atualização de Branches

Sempre tente atualizar suas branches utilizando `rebase`, isso vai nos ajudar a ter um histórico de commits
mais limpo e organizado.

## Commits

Para criar bons commits, evite adicionar alterações não relacionadas em um mesmo commit, e sempre utilize
a mensagem de commit para descrever o que foi feito, evite coisas como "Fix bug" ou "Improve service",
mensagens como essas não dizem o que as alterações do commit fazem, um bom exemplo seria "Fix bug when sending
a video message".
