Configurando o editor de código
===============================

Nesta seção mostraremos práticas e configurações para que você possa seguir o nosso code style.

## Legibilidade

Evite linhas de código muito grandes, o ideal é que você possa ler a linha inteira sem precisar
mover o editor para a direita. Acreditamos que o ideal seja uma linha com no máximo 90 caracteres,
se usar os nossos linters, eles vão te avisar quando você ultrapassar esse limite, caso contrário,
você pode configurar o seu editor de código para te ajudar a identificar o tamanho da sua linha:

### VS Code

Aperte `CTRL + Shit + P`, busque por `Open Settings (JSON)` e adicione essa linha no seu arquivo
de configuração:
```json
"editor.rulers": [90],
```
Você vai perceber que duas linhas verticais vão ser renderizadas, elas vão te ajudar a ficar dentro
do limite de tamanho.

## Indentação

Utilize sempre espaços ao invés de tabs (\t), e configure o número de espaços para 2:

### Atom

Certifique que você tem o Soft Tabs habilitado e o Tab Length definido como 2.

### SublimeText

Edite suas preferências (`⌘ + , / Ctrl + ,`) adicionando:

  * `tab_size` como `2`
  * `translate_tabs_to_spaces` como `true`
  * `use_tab_stops` como `true`

### Vim

No seu `~/.vimrc` adicione:

  * `set ts=2 sts=2 sw=2 expandtab`
  * `set autoindent`

### VS Code

Entre nas configurações (`⌘ + , / Ctrl + ,`) e defina:

  * `Auto Indent` como `full`
  * `Tab Size` como `2`
  * E marque `Insert Spaces`

## Remoção de espaços em branco

Configure o seu editor de código para remover espaços em branco
desnecessários:

### Atom

Certifique que você tem o pacote whitespace instalado e a sua opção
`Remove Trailing Whitespace` habilitada.

### SublimeText

Defina a opção `trim_trailing_white_space_on_save` como `true`.

### Vim

No seu `~/.vimrc` adicione:

```
autocmd BufWritePre * :%s/\s\+$//e
```

Isso vai remover os espaços em branco ao salvar os arquivos.

### VS Code

Marque a opção `Trim Trailing Whitespace`.

## Linters

Recomendamos utilizar alguns linters para que seja mais fácil seguir
o nosso code style, utilizamos o Rubocop para Ruby e ESlint e Prettier
para Javascript, instale o necessário para o seu trabalho:

### VS Code

#### Rubocop

Aperte `CTRL + SHIFT + X`, busque e instale o `ruby-rubocop`
