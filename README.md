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
**Git clone**  
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

### Observação importante 
Os comandos apresentados aqui são só uma parte dos comandos do Git, mas com certeza são os mais importantes e os que você mais vai usar no seu dia a dia como pessoa desenvolvedora, então não esqueça de particar bastante e sempre que precisar pode voltar aqui para relembrar os comandos e também para me ajudar a melhorar essa página e suas informações, ok. 😊
Suas criticas, observações e ou comentários são sempre bem vindos! 👊
