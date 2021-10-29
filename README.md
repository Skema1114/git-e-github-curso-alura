# GitGithubCursoAlura

## Neste projeto:

- Primeiro curso:

  - Git e Github: Controle e compartilhe seu código
  - https://cursos.alura.com.br/course/git-github-controle-de-versao

- Segundo curso:

  - Git e Github: Estratégias de ramificação, Conflitos e Pull Requests
  - https://cursos.alura.com.br/course/git-github-branching-conflitos-pull-requests

## Comandos utilizados

- `git init` [dentro de clone-server-repo, remote-server-repo] (inicializa o git)
- `git status` (verificar o status do repositório)
- `git add imdex.html / index add .` (adicionar um ou vários arquivos para que o git comece a "escutá-lo" e que o mesmo fique pronto para receber uma mensagem de commit)
- `git commit -m "Mensagem pequena e descritiva"` ("encapsula" os arquivos que estão sendo "escutados"/estagiados e rotula os mesmos com essa mensagem passada)
- `git log` (mostra diversas informações do histórico de commits efetuados no repositório)
- `git config --local user.name "Nome"` (altera o nome do usuário no repositório)
- `git config user.name` (visualiza o nome do usuário no repositório)
- `git log --oneline` (mostra o log só que de forma super resumida)
- `git log -p` (mostra o log só que de forma super completa)
- `git log --pretty="format:%H"` (indenta para que o log mostra apenas os hashes dos commits)
- `git log --pretty="format:%h %s"` (indenta o log de forma que o mesmo mostre apenas o hash resumido o as mensagens de commits)
- `git log --pretty="format:%h %s %ae"` (indenta o log de forma que o mesmo mostre apenas o hash resumido, as mensagens de commits e o email do autor)
- `git init --bare` [dentro de server-repo] (informa que esse repositório só vai servir para armazenar as alterações dos arquivos e não os arquivos propriamente dito, um repositório "puro")
- `git remote` (lista os repositórios remoto que o repositório local conhece)
- `git remote add server-repo C:\projetos\git-e-github-curso-alura\repo\server-repo` [dentro de clone-server-repo, remote-server-repo] (adicionando um repositório remoto na pasta atual, onde o nome do mesmo foi colocado como server-repo e por último foi passado o caminho do servidor)
- `git remote -v` (mostra o endereço dos repositórios remotos)
- `git clone C:\projetos\git-e-github-curso-alura\repo\server-repo projeto` (clonando o repositório remoto servidor dentro da pasta atual e nomeando esta pasta para projeto)
- `git add .\local-to-remote-server-repo.html` [denro de remote-server-repo]
- `git commit -m "Enviando para o server-repo"` [dentro de remote-server-repo]
- `git push server-repo master` [dentro de remote-server-repo]
- `git pull server-repo master` [dentro de clone-server-repo]
- `git remote rename nomeAntigo novoNome` (para renomear um determinado remote)
- `git push -u origin master` (o -u do comando faz com que, você está 'dizendo' que sempre que estiver na master do origin, pode fazer apenas o 'git pull' e não o comando inteiro, ele cria tipo um atalho)
- `git branch titulo`
- `git checkout titulo`
- `git merge titulo` [dentro da branch master] (cria um novo commit na branch atual e atualiza/junta com os dados da branch titulo (neste exemplo))
- `git rebase titulo` [dentro da branch master] (o git vai pegar os commits da branch titulo e atualizar junto do commit novo na branch master, ele vai pegar esse commit novo da branch master e trazer para frente de todos, ou seja, gerará um novo commit. Com isso, a branch master fica com todos os commits que estavam na branch titulo e junto com o novo que tinha na master)
- `git log --graph` (mostra as linhas de desenvolvimento dos commits)
- `git checkout -- index.html` (para desfazer alguma modificação não estagiada (não marcadas para commitar), pode-se realizar esse comando, no exemplo está voltando o mesmo para desfazer as alterações do arquivo index.html, pode-se notar que o checkout serve para andar entre estados, tanto nas branches como nos estados de edições)
- `git reset HEAD index.html` (desmarca o arquivo passado para não entrar no commit, ou seja desestagia aquele determinado arquivo)
- `git revert 0c109eb38d46a218dc00f935225bee8d596de169` (para reverter/desfazer uma modificação que já foi commitada, basta adicionar este código passando o hash do commit que precisa ser desfeito, pode ser passado o hash menor)
- `git stash` (salvar as alterações em um lugar temporário sem fazer o commit)
- `git stash list` (lista os stashes salvos)
- `git stash apply 0` (para pegar uma stash da lista, basta adicionar esse comando e passar o numero daquela determinada stash desejada, só que assim a stash ainda continuará na lista de stash, mesmo após a chamada da mesma)
- `git stash drop 0` (apaga a stash informada baseado no número da mesma obtido pela lista de stashes)
- `git stash pop` (pega a última stash da lista, faz um merge nas modificações atuais e ao mesmo tempo remove essa stash da lista)
- `git checkout 7723960` (viaja para um commit em específico, você fica desanexado do HEAD e não está em uma branch especifica, pode ser feitas modificações e alterações e quando voltar para master, as alterações serão ignoradas)
- `git checkout -b novo-branch` [dentro do commit solto 7723960 (baseado no código de cima)] (agora será criada uma nova branch levando em consideração como aquele commit estava, ai sim as alterações commitadas serão salvas)
- `git diff 7723960..87fef94` (com esse comando é possível verificar as alterações de um determinado commit até (no código, o até é passado como os 2 pontinhos (..)) outro commit)
- `git diff` (Mostra o que tem para estagiar, ou seja, para adicionar no commit, mas depois que foi adicionado, ele nao mostrar-a nada)
- `git tag -a v0.1.0` (cria uma tag, uma versão do código que não poderá ser alterada, as alterações feitas entrarão na próxima tag criada)
- `git tag -a v0.1.0 -m "Lançando a primeira versão (BETA) da aplicação de cursos"` (cria uma tag/versão e adiciona uma mensagem na mesma)
- `git tag` (mostra todas as tags que o repositório possui)
- `git push origin v0.1.0` (envia para o repositório remoto a tag/versão criada localmente)
- `git rebase -i HEAD~3` (faz a união de commits, tornando-os em um único, com esses parâmetros significa que a partir do momento atual (agora, para onde o HEAD ta apontando), eu quero unir os outros 3 commits anteriores)
- `git rebase -i bdae6f0` (faz a união de commits, tornando-os em um único, nesse codigo foi passado o commit anterior aos que eu quero unir, ou seja, é escolhido um antes dos desejados)
- `git cherry-pick 5c9e3e4` (traz o commit selecionado para o banch atual)

## Anotações

- `HEAD:` Estado atual do nosso código, ou seja, onde o Git os colocou;
- `Working tree:` Local onde os arquivos realmente estão sendo armazenados e editados;
- `index:` Local onde o Git armazena o que será commitado, ou seja, o local entre a working tree e o repositório Git em si;
- **OBS:** Para sair do `(END)` no windows (testado no `Poweshell`) basta pressionar a tecla `q`;
- **CONVENÇÃO/CONSENSO:** VOCÊ NUNCA DEVE COMMITAR UM CÓDIGO QUE NÃO FUNCIONA, O CÓDIGO TEM QUE ESTAR EM ESTADO FUNCIONAL PARA SER COMMITADO;
- **DICA DO CURSO:** Devemos gerar um commit sempre que a nossa base de código estiver em um estado do qual gostaríamos de nos lembrar. Nunca devemos ter commits de códigos que não funcionam, mas também não é interessante deixar para commitar apenas no final de uma feature. Essa pode ser uma discussão sem fim e cada empresa ou equipe pode seguir uma estratégia diferente. Estude sobre o assunto, entenda o que faz mais sentido para você e sua equipe e seja feliz;
- **DICA SHOW:** Sempre antes de fazer um commit, é necessário verificar se aquela determinada branch está atualizada ou seja, se possuímos a última versão da mesma;
- **OBS:** No editor tipo do merge fail, que pode alterar as mensagens de commit no editor do terminal, para sair basta adicionar o comando `:x`;
- **DO CURSO:** Com o git checkout nós desfazemos uma alteração que ainda não foi adicionada ao index ou stage, ou seja, antes do git add. Depois de adicionar com git add, para desfazer uma alteração, precisamos tirá-la deste estado, com git reset. Agora, se já realizamos o commit, o comando git revert pode nos salvar;
- **OBS:** No git `rebase -i [hash]` após definir os commits que serão unidos, aparecerá uma tela que você tera de escolher quais commits serão unidos em quais, ou seja, deve deixar coemçar com a palavra `pick` aquele commit que receberá os outros commits (geralmente o primeiro da lista pois foi o último commitado) e nos outros é trocado a palavra `pick` pela letra `s`, onde todos que tiverem `s` serão unidos ao `pick` e por fim, após presionar `esc` e escrever `:x` para salvar, será mostrada uma outra tela e nesta será adicionada a mensagem de commit.

## Entendendo

- Status commits
  <img src="assets\img\status-commits.png" width="auto">

## Links

- Comandos e parâmetros disponíveis do git log (`https://devhints.io/git-log`)
- Formatando os logs com o prettie (`https://devhints.io/git-log-format`)
- Visualizando graficamente como os comandos do git funcionam (`https://git-school.github.io/visualizing-git/#free`)
- Apresentação sobre software livre (`https://slides.com/daianealvesrj/software-livre-para-empreendedores`)
