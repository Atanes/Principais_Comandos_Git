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
