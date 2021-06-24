# GitEGithubCursoAlura

## Neste projeto:

- Curso:

  - Git e Github: Controle e compartilhe seu código
  - https://cursos.alura.com.br/course/git-github-controle-de-versao

## Comandos utilizados

- `git init` [dentro de clone-server-repo, remote-server-repo] (inicializa o git)
- `git status` (verificar o status do repositório)
- `git add imdex.html / index add .` (adicionar um ou vários arquivos para que o git começe a "escutá-lo" e que o mesmo fique pronto para receber uma mensagem de commit)
- `git commit -m "Mensagem pequena e descritiva"` ("encapsula" os arquivos que estão sendo "escutados"/estageados e rotula os mesmos com essa mensagem passada)
- `git log` (mostra diversas informações do histórico de commits efetuados no repositório)
- `git config --local user.name "Nome"` (altera o nome do usuário no repositório)
- `git config user.name` (visualiza o nome do usuario no repositório)
- `git log --oneline` (mostra o log só que de forma super resumida)
- `git log -p` (mostra o log só que de forma super completa)
- `git log --pretty="format:%H"` (indenta para que o log mostre apenas os hashs dos commits)
- `git log --pretty="format:%h %s"` (indenta o log de forma que o mesmo mostre apenas o hash resumido o as mensagens de commits)
- `git log --pretty="format:%h %s %ae"` (indenta o log de forma que o mesmo motre apenas o hash resumido, as mensagens de commits e o email do autor)
- `git init --bare` [dentro de server-repo] (informa que esse repositorio so vai servir pra armazenar as alterações dos arquivos e não os arquivos própriamente dito, um repositório "puro")
- `git remote` (lista os repositorios remoto que o repositorio local conhece)
- `git remote add server-repo C:\projetos\git-e-github-curso-alura\repo\server-repo` [dentro de clone-server-repo, remote-server-repo] (adicionando um repositório remoto na pasta atual, onde o nome do mesmo foi colocado como server-repo e por ultimo foi passado o caminho do servidor)
- `git remote -v` (mostra o endereço dos repositorios remotos)
- `git clone C:\projetos\git-e-github-curso-alura\repo\server-repo projeto` (clonando o repositorio remoto servidor dentro da pasta atual e nomeando esta pasta para projeto)
- `git add .\local-to-remote-server-repo.html` [denro de remote-server-repo]
- `git commit -m "Enviando para o server-repo"` [denro de remote-server-repo]
- `git push server-repo master` [dentro de remote-server-repo]
- `git pull server-repo master` [dentro de clone-server-repo]
- `git remote rename nomeAntigo novoNome` (para renomear um determinado remote)
- `git push -u origin master` (o -u do comando faz com que, você está 'dizendo' que sempre que estiver na master do origin, pode fazer apenas o 'git pull' e não o comando inteiro, ele cria tipo um atalho)
- `git branch titulo`
- `git checkout titulo`
- `git merge titulo` [dentro da branch master] (cria um novo commit na branch atual e atualiza/junta com os dados da branch titulo (nese exemplo))
- `git rebase titulo` [dentro da branch master] (o git vai pegar os commits da branch titulo e atuaizar junto do commit novo na branch master, ele vai pegar esse commit novo da branch master e trazer para frente de todos, ou seja, gerará um novo commit. Com isso, a branch master fica com todos os commits que estavam na branch titulo e junto com o novo que tinha na master)
- `git log --graph` (mostra as linhas de desenvolvimento dos commits)
- `git stash apply 0` (para pegar uma stash da lista, basta adicionar esse comando e passar o numero daquela determinada stash desejada, só que assim a stash ainda continuará na lista de stash, mesmo após a chamada da mesma)
- `git stash drop 0` (apaga a stash informada baseado no numero da mesma obtido pela lista de stashs)
- `git stash pop` (pega a ultima stash da lista, faz um merge nas modificações atuais e ao mesmo tempo remove essa stash da lista)

## Anotações

- `HEAD:` Estado atual do nosso código, ou seja, onde o Git os colocou;
- `Working tree:` Local onde os arquivos realmente estão sendo armazenados e editados;
- `index:` Local onde o Git armazena o que será commitado, ou seja, o local entre a working tree e o repositório Git em si;
- **OBS:** Para sair do `(END)` no windows (testado no `Poweshell`) basta pressionar a tecla `q`;
- **CONVENÇÃO/CONSENSO:** VOCÊ NUNCA DEVE COMMITAR UM CÓDIGO QUE NÃO FUNCION, O CÓDIGO TEM QUE ESTAR EM ESTADO FUNCIONAL PARA SER COMMITADO;
- **DICA DO CURSO:** Devemos gerar um commit sempre que a nossa base de código está em um estado do qual gostaríamos de nos lembrar. Nunca devemos ter commits de códigos que não funcionam, mas também não é interessante deixar para commitar apenas no final de uma feature. Essa pode ser uma discussão sem fim e cada empresa ou equipe pode seguir uma estratégia diferente. Estude sobre o assunto, entenda o que faz mais sentido para você e sua equipe e seja feliz;

## Entendendo

- Status commits
  <img src="assets\img\status-commits.png" width="auto">

## Links

- Comandos e parâmetros disponíveis do git log (`https://devhints.io/git-log`)
- Formatando os logs com o prettie (`https://devhints.io/git-log-format`)
- Visualizando graficamente como os comandos do git funcionam (`https://git-school.github.io/visualizing-git/#free`)
