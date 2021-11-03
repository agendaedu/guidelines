Fluxo de trabalho
=================

Nessa sessão vamos explicar nosso processo de criação de epics e cards/tasks no Jira, assim como seus tipos e
estados.

## Epics

Qualquer modificação no produto que é grande ao ponto de não poder ser feita em uma única task, é uma epic,
podendo realmente alterar o produto, como implementar uma nova feature, ou sendo imperceptível ao usuário,
como atualizar dependências.

## Tasks

Cada task no Jira pode variar o tipo e pode ou não pertencer a uma epic. Geralmente nossas tasks variam dentre
os seguintes tipos:

### Feature
Algo novo que precisa ser implementado. Exemplos:

- Implementar service de atualização de consumo de dados
- Fazer botão de aumento de limite
- Criar componente da barra de consumo

Geralmente, esse tipo de task pertence a uma epic, e o título terá o verbo "Criar", "Implementar" ou "Fazer".

### Bug
Algo não está funcionando como deveria em produção. Exemplos:

- Não é possível remover anexo em Plano de Aula
- Alunos estão sendo duplicados ao ter o diário preenchido
- Todos os selects do Form de Diário estão como required

Só consideramos bug algum problema em produção, portanto, bugs não pertencem a epics. Geralmente, o título já
vai informar o problema que precisa ser resolvido.

### Enhancement
Algo precisa ser melhorado ou ajustado. Exemplos:

- Mover informação de limite de armazenamento para o código
- Alterar permissões padrão dos professores
- Adicionar suporte a mais formatos de vídeos em mensagens

### Tech task
Manutenções no projeto que na maioria das vezes são imperceptíveis ao usuário. Exemplos:

- Atualizar Moment.js
- Ajustar configuração do CircleCI
- Alterar a chave de criptografia do banco de dados

### Back and forth
Problemas encontrados após bateria de testes em uma epic. Exemplos:

- Família (aluno e responsável) consegue enviar .ogv e .webm
- Mensagens de multimédia enviadas por alunos e responsáveis estão impactando no consumo da escola
- Erro 500 ao acessar a 'Minha conta' no equipe

Observe que esse tipo de task é muito parecida com os bugs, com a diferença que bugs estão em produção,
enquanto que um back and forth é um "bug" que está na epic, ou seja, que ainda não está em produção.

### Suport
Tasks que representam demandas vindas do time de suporte. Exemplos:

- Excluir mensagem enviada pelo responsável
- Recuperar mensagens excluídas pela plataforma
- Atualizar em massa os assessores das escolas

## Criando uma boa task
Para que o seu trabalho e do seu time fluam bem, é fundamental que as tasks sejam bem cadastradas,
observamos que tasks bem descritas melhoram muito o cycle time.

### Título
No título, tente passar um resumo do que precisa ser feito, você pode usar o seguinte template
[Verbo] [O quê] [Onde]:

- Ajustar configuração do CircleCI
- Alterar permissões padrão dos professores
- Implementar service de atualização de consumo de dados

OBS.: O "onde" não precisa ser colocado em tasks de feature, já que nessas tasks o "onde" será criado.

### Descrição
É na descrição que devemos colocar todas as informações necessárias para a task. O que precisa ser colocado na
descrição vai variar de task para task, e você pode usar os tópicos abaixo como guia:

- Escopo/O que precisa ser feito: A menos que a task seja extremamente simples, é fundamental que você detalhe o
que precisa ser feito.
- Motivo da task: Ninguém gosta de trabalhar em algo sem sentido, certo? Então colocar o motivo da task ajuda
as pessoas entenderem o porquê aquilo precisa ser feito.
- Exemplos/Sugestões de como fazer: Se você já resolveu um problema parecido, compartilhe sua experiência com o seu
time, isso pode agilizar muito o trabalho de uma pessoa menos experiente.
- Arquivos que precisaram ser alterados: Se você já sabe quais arquivos precisam ser alterados, coloque essa
informação na descrição, isso também pode agilizar muito o trabalho de quem pegar a task.

Boas descrições exigem um pouco mais de esforço, mas encare isso como um investimento, você gastará um pouco mais de tempo
agora, para que a task possa ser concluída em menos tempo.

## Estados de uma task

Dentro do board do Jira, o card de uma task vai sempre estar em uma coluna, onde a coluna representa o seu estado:

- Sprint backlog: Tirando tasks do tipo back and forth, todos os cards de tasks pendentes ficarão nessa coluna.
- In progress: Significa que alguém está trabalhando na task.
- Blocked: Não podemos dar andamento na task por algum motivo. Exemplo: a API externa x está indisponível.
- Back and forth: Tasks do tipo back and forth que estejam pendentes ficam nessa coluna.
- Design review: Tasks que estejam aguardando ou passando por um design review ficam localizadas aqui.
- Testing: Tasks que estejam aguardando ou passando por testes ficam localizadas aqui.
- Code review: Tasks que estejam aguardando ou passando por um code review ficam localizadas aqui.
- To deploy: Quando uma task está pronta para ser enviada para produção, ela é colocada nessa coluna.
- Done: Lugar das tasks concluídas
