# Principais Comandos do Git
Lista dos principais comandos do GIT e alguns exemplos de uso desses comandos

## Objetivo
Apresentar os principais comandos do GIT com exemplos práticos de sua utilização no dia a dia

### Tecnologias/Ferramentas Utilizadas
Git, GitHub, Git Bash, VSCode

Antes de começar é importante que você tenha o Git, o Git Bash (faz parte da instalação do Git) e o VSCode instalados na sua máquina e por isso estpu adicionando aqui alguns sites com as informações e procedimentos para essas instalações, ok! 😉

[Git / Git Bash](https://git-scm.com/book/pt-br/v2/Come%C3%A7ando-Instalando-o-Git)  
[VSCode](https://code.visualstudio.com/docs)

### Comandos
**git config**
 - Quando utilizamos o Git pela primeira vez ou em uma instalação nova, em um projeto colaborativo (onde estamos trabalhando com outras pessoas), esse comando é fundamental para configurar sua identidade de usuário, inserindo informações como nome e email que serão empregadas em cada commit que você realizar.

Exemplo:
```
$ git config –global user.name “seu-nome-de-usuario”

$ git config –global user.email “seu-email@email.com”
```

**git init**
 - Esse é o comando que utilizamos para criar um novo projeto em um repositório controlado pelo git. O comando irá criar um repositório novo em branco e, a partir daí, será possível armazenar seu código fonte, alterar, salvar e gerenciar todas as alterações feitas nesse repositório.
 - Esse comando cria um novo subdiretório chamado .git que contém todos os arquivos necessários de seu repositório – um esqueleto de repositório Git.

Exemplo:
```
$ git init
```
Se você já possui um repositório anterior ou deseja criar um repositório com um nome em específico, você pode passar o nome como parâmetro do comando:
```
$ git init <O nome do seu repositório>
```
<p align='center'>
  <img src='https://user-images.githubusercontent.com/18126923/206562380-f49d7da4-b5d3-4ccb-9bca-f6bc5f129555.png'><br>
  Criando um repositório local gerenciado pelo git
</p>

**git clone**  
 - Git clone é um comando que faz uma cópia (clone) de um repositório remoto para a sua máquina local ou outra máquina que você deseje, com ele você consegue baixar todo o código-fonte existente em um repositório remoto (como, por exemplo, o Github ou Bitbucket) para a sua máquina sem muitas dificuldades e o repositório local vai ficar exatamente com a mesma estrutura, código e histórico do repositório remoto. Em resumo, utilizamos o git clone, basicamente, para fazer uma cópia idêntica da versão mais recente de um projeto em um repositório remoto para outra máquina.

Existem algumas maneiras difirentes de clonar o repsotório com esse comando, mas com certeza as mais utilizadas são via https ou SSH:
```
git clone https://github.com/Atanes/controle-estoque.git
```
```
git clone git@github.com:Atanes/controle-estoque.git
```

Por exemplo, se eu quiser baixar um projeto do Github, tudo que você precisa fazer é clicar no botão Code ou Código, selecionar como quer fazer o clone, via HTTPS, SSH ou via Git CLI, copiar o URL da caixa logo abaixo e colá-lo após o comando git clone no seu terminal.
<p align='center'>
  <img src='https://user-images.githubusercontent.com/18126923/206558597-3ea60c0a-8810-4dd3-bbf8-b2b57a39bcb4.png'><br>
  Exemplo com o código-fonte de um projeto no Github
</p>
<p align='center'>
  <img src='https://user-images.githubusercontent.com/18126923/206559065-39a066fe-89ab-481d-b663-715a50ee6bd0.png'><br>
  Esse comando vai criar uma cópia do projeto na sua máquina de trabalho local onde você vai poder trabalhar sem problemas.
</p>

**git branch**  
 - Durante o desenvovlimento de um sistema é comum, na maior parte do tempo, trabalharmos em múltiplos "workspaces" dentro do nosso repositório Git, chamamos esses "workspaces" de branches (“ramificações”). De forma geral um branch é uma aréa independente de desenvolvimentodentro do seu sistema/projeto.

Em um primeiro momento pode parecer entender esses vários "workspaces" e se perder com o controle deles, mas o comando git branch facilita esse gerenciamento e simplifica muito nosso controle sobre essas "ramificações de trabalho". Com diferentes parâmetros, é possível listar, criar, renomear e ou apagar os branches do seu sistema/projeto.

Para listar todas as branchs existentes é só usar o git branch:
```
git branch
```
Para incluir uma nova branch é só usar o git branch + o nome da branch:
```
git branch nova-branch
```
Para remover uma branch utilizamos o parametro -d depois do git branch:
```
git branch -d nome-da-branch
```
Para renomear uma branch existente utilizamos o parametro -m no comando git branch:
```
git branch -m nome-antigo novo-nome
```
<p align='center'>
  <img src='https://user-images.githubusercontent.com/18126923/208152092-7a8e9d5f-229b-4562-9fbf-fd9b5ae87d5c.png'><br>
  Utilização do git branch
</p>

**git checkout**  
 - Esse com certeza é um dos comandos mais utilizados no Git, pois para trabalhar em uma branch, primeiro, é preciso estar "dentro" dela. Usamos git checkout, na maioria dos casos, para trocar de uma branch para outra, esse comando também pode ser usado para fazer o checkout de arquivos e commits que vamos ver mais adiante.

Para "entrar" uma branch:
```
git checkout nome-da-branch
```
O comando git checkout também nos permite criar e automaticamente trocar para a branch criada ao mesmo tempo:
```
git checkout -b nome-da-branch
```
Esse comando cria a branch nova no seu workspace local, a flag -b indica para o git que é uma nova branch, e faz o checkout para a nova branch logo após sua criação.

Uma observação importante é que existem alguns passos que precisam ser seguidos para trocar de branch sem problemas:
  1. As alterações em sua branch atual devem estar em um commit ou em um stash antes de você fazer a troca
  2. A branch na qual você quer fazer o checkout deve existir no seu espaço de trabalho local

**git add**  
 - Quando você inicia um repositório via git clone ou git init, todos os seus arquivos passam a ser monitorados e controlados pelo Git. Conforme você edita esses arquivos e ou inclui novos arquivos no seu projeto, o Git passa a vê-los como modificados, porque você fez alguma alteração/inclusão desde seu último commit. Para registrar essas alterações e fazer um commit com as informações das alterações antes você precisa usar o git add para "incluir" os arquivos novos/alterados na area de "stage" do git antes de "registrar" as mudanças com o git commit que vamos ver em seguida.

Para incluir um arquivo especifico é preciso determinar o nome do arquivo novo/modificado depois do git add:
```
git add index.html
```
Para incluir todos os novos arquivos e ou arquivos modificados de uma unica vez você pode usar o "." depois do git add:
```
git add .
```

**git status**
 - O comando git status te mostra todas as informações necessárias sobre quais arquivos estão em quais estados na branch atual.
 Com esse comando é possivel verificar se algum arquivo foi alterado, se está na area de stage pronto para receber um commit entre outras coisas.
```
git status
```
<p align='center'>
  <img src='https://user-images.githubusercontent.com/18126923/208154067-bfe921f2-add8-412f-a6b3-5567ac089324.png'><br>
  Exemplos de informações geradas pelo comando do git status
</p>

**git commit**
 - Com certeza esse é um dos comandos mais utilizado no Git. Depois de algumas modificações, inclusão de novos arquivos, quando chegamos a determinado ponto do nosso desenvolvimento onde queremos manter um histórico e criar um "ponto de controle", podemos definir uma "marca" de verificação com o git commit. Com essa "marca" é possivel voltar até esse ponto mais tarde se for necessário.
O git commit salva efetivamente as modificações no seu workspace e coloca uma "marca", um tag de controle naquele ponto do desenvolvimento que pode ser consultado, comparado com outros pontos de alteração e ou utilizado para fazer um rollback do código em caso de problemas mais sérios.
Observação: É necessário inserir uma mensagem breve para explicar/indentificar o que desenvolvemos ou alteramos no código-fonte naquele momento.
```
git commit -m "inclusão de novos arquivos de controle"
```
Nesse ponto também é importante entender as diferenças entre o git add e o git commit:

git add é utilizado para adicionar os modificações realizadas à area de stage (fila de controle) do git para serem submetidos a um commit posteriormente. Os arquivos que ainda não passaram por um commit.
O git commit salva efetivamente as alterações e cria uma nova revisão com um log para esse conjunto de alterações que foram adicionadas na area de stage pelo git add.
Você pode combinar os dois comandos (git add e git commit) utilizando o parametro -a no comando commit:
```
git commit -a -m "inclusão de novos arquivos de controle"
```
Dessa forma o git adiciona todas modificações pendentes a area de stage e logo em seguida efetiva o commit sobre essas alterações.
<p align='center'>
  <img src='https://user-images.githubusercontent.com/18126923/208159181-3d93b10b-15b1-432f-80fe-e87753154b8e.png'><br>
  Utilização do git commit
</p>

**git push**
 - Após confirmar as alterações com o git commit que você fez na sua máquina local é necessário fazer o envio das alterações para o seu servidor remoto para deixa-lo atualizado em relação as essas alterações e para isso usamos o comando git push:
```
git push <remote> <nome-do-branch>
git push origin novas-features
```
Obs: Caso sua branch tenha sido criada localmente, você também precisará fazer upload da branch utilizando a parametro **-u** junto com git push:
```
git push -u origin <nome-do-branch>
```

**git pull**
 - O git pull faz o caminho inverso do git push, ou seja, é utilizado para se obter atualizações do repositório remoto. 

Este comando é uma combinação de git fetch (baixa as alterações do repositório remoto, mas não faz o merge com o seu repositório local) e git merge (que faz o merge efetivo dos repositórios para uma branch especifica).

Isso significa que, quando usamos o git pull, ele recebe as atualizações do repositório remoto (git fetch) e aplica imediatamente as alterações mais recentes no seu repositório local (git merge).
Para baixar todas as atualizações existentes no repositório remoto:
```
git pull <remote>
```
Para baixar todas as atualizações existentes no repositório remoto em uma branch especifica:
```
git pull <remote> <nome-da-branch>
```
<p align='center'>
  <img src='https://user-images.githubusercontent.com/18126923/211423254-dcdebb52-ca6c-4555-b1dc-8ad03815bbe8.png'><br>
</p>

**git merge**
 - Após concluir o desenvolvimento em sua branch e fazer os testes necessários para verificar se tudo está funcionando bem, a próxima etapa é mesclar as suas alterações com a branch principal do projeto (por exemplo), isso é feito através do comando git merge.
Esse comando integra as mudanças de duas branches diferentes em uma única branch. Ele precisa ser executado a partir de um branch especifica, que será mesclada com outra que é passada por parâmetro no comando.
```
git merge <nome-da-branch>
```
No exemplo abaixo a branch **resolucao-atanes** vai receber todas as alterações e atualizações existentes na branch main:
<p align='center'>
  <img src='https://user-images.githubusercontent.com/18126923/211422747-43c7ecee-96fa-4f91-b206-6b6559abee1d.png'><br>
</p>

### O ciclo de vida dos status dos arquivos no Git
<p align='center'>
  <img src='https://git-scm.com/book/en/v2/images/lifecycle.png'><br>
</p>

Referência: [GIT-SCM](https://git-scm.com/book/pt-br/v2/Fundamentos-de-Git-Gravando-Altera%C3%A7%C3%B5es-em-Seu-Reposit%C3%B3rio)

### Observação importante 
Os comandos apresentados aqui são só uma parte dos comandos do Git, mas com certeza são os mais importantes e os que você mais vai usar no seu dia a dia como pessoa desenvolvedora, então não esqueça de particar bastante e sempre que precisar pode voltar aqui para relembrar os comandos e também para me ajudar a melhorar essa página e suas informações, ok. 😊
Suas criticas, observações e ou comentários são sempre bem vindos! 👊
### Comandos adicionais
Caso queria ver os demais comandos e ou precisar de um **help** com algum comando você pode usar o git help sem medo, ok! 😉
```
git help
```
<p align='center'>
  <img src='https://user-images.githubusercontent.com/18126923/206564169-38b8d270-eec1-4169-ba8d-566766dc876c.png'><br>
  Lista de comandos do git com ajuda do git help
</p>
