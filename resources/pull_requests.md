Pull Requests
=============

Pull Request (PR) é uma maneira de incluir mudanças em um repositório do GitHub onde um contribuidor
pede para algumas pessoas revisarem o seu código e após um determinado número de aprovações
a mudança é aplicada no repositório. PRs tem vantagens bem interessantes, como:

- Ajuda o time a saber o que está sendo alterado
- Facilita a colaboração de pessoas desenvolvedoras para entregar um código de maior qualidade
- Facilita a disseminação de conhecimento
- Ajuda a documentar alterações

Por conta de todas essas vantagens, toda alteração, independente do repositório, deve ser feita por
meio de um PR.

## Abrindo Pull Requests

### Título

Os títulos devem seguir o seguinte padrão:

```
[Código da epic][Código da task] Título da task do Jira
```

Exemplo:
```
[SE-3443][SE-3444] Criar endpoint de consumo de dados
```

### Descrição

A descrição do seu PR precisa responder duas perguntas:

- Qual o objetivo do seu PR?
- O que você fez para atingir o objetivo?

Você sabe que a sua descrição está boa quando até uma pessoa de fora do seu contexto consegue revisar
o seu PR.

### Etiquetas

Utilizamos etiquetas para organizar os nosso PRs, sempre adicione etiquetas que tem relação com o seu PR.

### Revisores

Sempre que abrir um PR, você vai precisar marcar algumas pessoas para revisar o seu código, é necessário ao
menos duas aprovações para que o seu PR possa ser mesclado, baseado nisso, você pode chamar 3-5 pessoas, sendo
recomendável que uma delas seja de fora do seu contexto (outro squad, por exemplo).

### Assinaturas

A pessoa responsável pelo PR deve assiná-lo.

## Recebendo revisões

Nesse ponto, você já sabe como abrir um bom PR, no entanto, existem mais algumas práticas que você
pode aderir para melhorar as revisões que você vai receber, sempre que abrir um PR considere:

- Adicionar imagens ou vídeos: se o seu PR envolve mudanças visuais ou é uma correção de bug,
adicionar imagens ou vídeos pode ajudar muito na revisão.
- Fazer comentários sobre o código: você pode adicionar comentários no PR para explicar o porque
você seguiu uma determinada abordagem, ou até para ressaltar uma parte do código que você ainda
não está satisfeito, e assim guiar o seu review. No final das contas, ao comentar o seu PR você
estará documentando uma alteração no projeto, o que poderá ser bem útil no futuro.
- Leve sugestões e comentários como um aprendizado: sempre que alguém questionar ou pedir alterações
no seu código será com o objetivo de te ajudar a entregar a melhor solução possível, e não de fazer
você se sentir mal, portanto, sempre encare as revisões como uma oportunidade de evolução.

## Revisando Pull Requests

Além de receber, você também vai precisar revisar PRs, tanto de membros do seu squad quanto de fora.
Considere seguir as seguintes práticas sempre que precisar revisar algum PR:

- Procure por code smells: basicamente, code smells são padrões ruins de código que podem trazer problemas
no futuro, sempre que encontrar um code smell alerte a pessoa sobre o problema e se possível, mostre uma
alternativa. [Aqui](https://refactoring.guru/refactoring/smells) você pode aprender mais sobre o assunto.
- Compartilhe alternativas: sempre que possível compartilhe outras maneiras de atingir o objetivo colocado no PR.
- Sempre tire suas dúvidas: sempre que algo não estiver claro, pergunte, é muito importante que você tenha
entendido o problema e a solução antes de aprovar ou pedir alterações no código.
- Olhe os commits: certifique que a pessoa fez bons commits, caso contrário, alerte a pessoa sobre o problema.
- Verifique a existência de testes: adição ou alteração de comportamento sempre devem vir acompanhadas de uma boa
suite de testes, caso a pessoa não escreveu os testes, peça que ela faça isso.
- Busque a simplicidade: tente analisar o código da pessoa de modo a encontrar maneiras mais simples de resolver
o problema, caso encontre, faça uma sugestão de mudança.
- Aprecie um bom trabalho: caso não tenha encontrado nada para ser melhorado, isso é um sinal que o autor do PR
fez um bom trabalho, considere elogiar essa pessoa, pois isso pode incentivar ela a continuar entregando bom código.
